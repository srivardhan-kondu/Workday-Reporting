# WORKDAY SECURITY CERTIFICATION -- EXAM READINESS GUIDE

**Version:** 2026 Edition | **Print Format:** Black-and-White, A4-Optimised

---

> **How to Use This Guide**
>
> This guide is organised into four modules that mirror the certification
> exam blueprint. Each module contains a **Deep Dive** section covering
> the technical concepts you must master, followed by an **Examiner's Trap**
> section that highlights the most common reasons candidates fail that
> topic. Study every trap -- they are drawn from real exam feedback.

---

## TABLE OF CONTENTS

1. Core Security Architecture
2. Security Policies (The "Must-Knows")
3. Advanced Configuration and Inheritance
4. Examiner's Corner (Scenario-Based Questions)

---
---

# MODULE 1 -- CORE SECURITY ARCHITECTURE

---

## 1.1 Deep Dive

### The Workday Object Management System (OMS) and Its Relationship to Security

Workday stores everything -- workers, positions, organisations, compensation plans,
benefits, custom reports -- as **objects** inside a unified data model called the
**Object Management System (OMS)**. Unlike traditional ERP platforms that bolt
security onto an external directory, Workday's security is **intrinsic to the
object model itself**.

Key implications:

- **Every securable item in Workday is an object.** A report, a business
  process step, a web service endpoint, and even a dashboard widget are all
  OMS objects governed by the same security framework.

- **Security is evaluated at runtime.** When a user clicks a link, runs a
  report, or calls an integration, Workday traverses the OMS to determine
  which security groups the user belongs to, which security policies those
  groups are linked to, and whether the requested action is permitted. There
  is no static access-control list cached offline.

- **Security is tenant-wide and versionless.** All security configuration
  lives in the same tenant as the functional configuration. There are no
  separate "security databases." Changes to security policies follow the
  same activation workflow as other tenant configuration changes.

Understanding OMS means understanding that **you cannot discuss security without
discussing the data model**, and vice versa. The two are inseparable.

---

### Security Groups -- The Four Pillars

Workday classifies security groups into four primary types. Every security
assignment ultimately resolves to one or more of these types.

#### Comparison Table: Security Group Types

| Attribute | User-Based Security Group | Role-Based Security Group | Job-Based Security Group | Intersection Security Group |
|---|---|---|---|---|
| **Membership Basis** | Explicitly assigned users (manual list) | Users who hold a specific security role on an organisation or object | Users whose job profile, job family, or job family group matches the group criteria | Users who simultaneously belong to TWO OR MORE other security groups |
| **Constrained vs. Unconstrained** | Always **unconstrained** -- grants access to ALL instances of a secured domain | Can be **constrained** (access scoped to the specific organisation/object the role is assigned on) or **unconstrained** (access to all instances) | Can be **constrained** (access limited to own data or data related to the worker's position) or **unconstrained** | Inherits constraint behaviour from its component groups |
| **Common Use Case** | System administrators, integration system users, power users who need blanket access | Managers, HR Partners, Compensation Partners, Benefits Administrators -- anyone whose access should follow their organisational assignment | Self-service access (e.g., "all employees in the Analyst job family can view their own compensation") | Restricting a broad role to a narrow population (e.g., "HR Partners who are also in the EMEA region") |
| **Maintenance Overhead** | HIGH -- must manually add/remove users | LOW -- membership is automatic when the role is granted/revoked | LOW -- membership is automatic based on job data | MEDIUM -- must define the intersection logic and ensure component groups are current |
| **Exam Weight** | Moderate | Very High | Moderate | High |

---

#### Critical Terminology

- **Unconstrained:** The security group grants access to ALL instances of the
  secured data. Example: An unconstrained "View Compensation" group lets the
  member see compensation data for every worker in the tenant.

- **Constrained:** The security group grants access ONLY to instances related to
  the context in which the role is assigned. Example: A constrained "HR Partner"
  role assigned to the "North America" supervisory organisation lets the member
  see HR data only for workers in that organisation (and its subordinates, unless
  inheritance is blocked).

- **Functional Area:** A logical grouping of related security domains. Functional
  areas are used to organise the hundreds of domain and business process security
  policies into manageable categories (e.g., "Staffing," "Compensation,"
  "Benefits"). They do not grant access themselves; they are an organisational
  tool.

---

### Contextual Security and Supervisory Organisations

**Contextual security** is the mechanism by which a constrained security group
receives its scope. The "context" is the organisational node (most commonly a
**supervisory organisation**) on which a security role is assigned.

How it works:

1. An administrator assigns the "HR Partner" role to User A **on** the
   "Engineering -- US" supervisory organisation.
2. Because the "HR Partner" role uses a **constrained** role-based security
   group, User A can access HR data only for workers who are members of
   "Engineering -- US" and (by default) its subordinate organisations.
3. If User A also holds the "HR Partner" role on "Marketing -- EU," she
   gains HR data access for that branch as well. The two contexts are
   **additive** -- they do not interfere with each other.

The flow of security through supervisory organisations follows the organisation
hierarchy. The hierarchy defines:

- Which workers fall under which manager.
- Which constrained roles apply to which subset of the worker population.
- Where inheritance starts and where it can be broken (see Module 3).

**Key principle:** Supervisory organisations are the PRIMARY vehicle for
scoping constrained access. If a question on the exam mentions "context,"
think "supervisory organisation."

---

## 1.2 Examiner's Trap

**Trap 1: Confusing "Unconstrained" with "No Security"**

Candidates frequently assume that an unconstrained security group is less secure
than a constrained one. The exam tests whether you understand that
**unconstrained is a deliberate design choice** for roles that genuinely require
tenant-wide access (e.g., system administrators, integration accounts).
Choosing constrained vs. unconstrained is a scoping decision, not a
"more secure vs. less secure" decision.

**Trap 2: Forgetting Intersection Groups**

Many candidates memorise user-based, role-based, and job-based groups but
neglect intersection groups. The exam frequently presents a scenario where
a user's access must be restricted by BOTH role AND job profile. The correct
answer is almost always an intersection security group. If the question says
"must meet BOTH criteria," think intersection.

**Trap 3: Mixing Up "Functional Area" and "Domain"**

A functional area is a **container** for domains, not a permission itself.
The exam may offer an answer choice that says "assign the functional area
to the security group." This is always wrong. You assign **domains** (via
domain security policies) to security groups, and those domains happen to
be organised under functional areas for convenience.

---
---

# MODULE 2 -- SECURITY POLICIES (THE "MUST-KNOWS")

---

## 2.1 Deep Dive

### Domain Security Policies

A **domain security policy** controls access to a **security domain**, which
is a collection of related securable items (report fields, tasks, integration
data elements, etc.).

Each domain security policy defines two permission levels:

| Permission Level | What It Controls | Typical Assignment |
|---|---|---|
| **View** (Get) | Read-only access. The user can see data in reports, dashboards, and integrations but cannot change it. | Broad populations (e.g., all managers can view headcount data) |
| **Modify** (Put) | Read-write access. The user can view AND change data via tasks, data loads, and integration write-back. **Modify implicitly includes View.** | Narrow populations (e.g., only Compensation Partners can modify pay ranges) |

**Impact on Reports and Integrations:**

- A report field is visible to a user ONLY if the user's security groups are
  granted at least **View** access to the domain that contains that field.
  If even one field in a report is in a domain the user lacks access to, that
  field is suppressed (the rest of the report still renders).

- An outbound integration (e.g., EIB, Studio integration) can extract data
  only for domains to which the **Integration System User (ISU)** has View
  access. If the ISU lacks access, the field returns blank -- it does NOT
  throw an error by default.

- An inbound integration (e.g., data load via EIB) can write data only for
  domains to which the ISU has **Modify** access.

---

### Business Process Security Policies

A **business process (BP) security policy** controls WHO can perform WHICH
action within a business process. Unlike domain security, which governs data
visibility, BP security governs **workflow participation**.

The three distinct actions:

| Action | Meaning | Who Typically Holds It |
|---|---|---|
| **Initiate** | Start ("kick off") the business process. The initiator creates the event. | The worker (self-service), a manager, or an HR Partner |
| **Review** (legacy "View") | See the business process event details but NOT approve, deny, or send back. This is an observation-only step. | Auditors, security reviewers, downstream stakeholders who need visibility |
| **Approve** (includes Deny, Send Back, Cancel) | Take action on a business process step -- approve, deny, send back, or cancel the event. | Managers, senior HR, compliance officers |

**Critical distinction from domain access:**

- Domain security asks: "Can this user SEE or CHANGE this piece of data?"
- BP security asks: "Can this user PARTICIPATE in this workflow, and in what
  capacity?"

A user might have domain-level View access to compensation data but lack the
BP security to initiate a compensation change. Conversely, a user might have
BP approval rights on a hire event but lack domain access to see the
candidate's background-check results within that event. **The two operate
independently.**

---

### Policy Activation -- The Critical Path

Editing a security policy does NOT make it effective. You must **activate**
the policy. The activation workflow is as follows:

**Step-by-step critical path:**

```
1. NAVIGATE to the security policy (domain or BP).
2. EDIT the policy -- add or remove security groups, change
   permission levels (View / Modify / Initiate / Approve).
3. SAVE the edits. At this point, the changes are in a
   "pending" state. They are NOT enforced.
4. NAVIGATE to "Activate Pending Security Policy Changes."
5. REVIEW the summary of all pending changes across the
   tenant.
6. CONFIRM activation. Workday records two timestamps:
   - "Pending" timestamp: when the edit was saved (Step 3).
   - "Active" timestamp: when the activation was confirmed
     (Step 6).
7. The policy is now ACTIVE and enforced for all users.
```

**What happens if you forget to activate?**

- The edited policy remains in a **pending** state indefinitely.
- The PREVIOUS version of the policy continues to be enforced.
- Users will NOT gain (or lose) any access based on the pending edits.
- There is **no automatic activation timer** and **no system alert** warning
  the administrator that changes are pending. The only way to discover
  un-activated changes is to run the "Activate Pending Security Policy
  Changes" task and review the pending summary.
- **Exam implication:** If a question describes a scenario where an
  administrator made security changes but users report no difference, the
  answer is almost certainly "the administrator forgot to activate the
  pending changes."

---

## 2.2 Examiner's Trap

**Trap 1: Assuming Modify Does Not Include View**

The exam will sometimes describe a user who can change data but supposedly
cannot see it. This is impossible. **Modify always includes View.** If a
question states that a user has Modify access, that user can also View the
data. Any answer choice that claims otherwise is incorrect.

**Trap 2: Confusing BP "Review" with Domain "View"**

These are NOT the same thing. BP "Review" is a workflow action that lets a
user observe a business process event. Domain "View" is a data-access
permission. The exam frequently presents answer choices that swap these terms.
Read the question carefully: is it asking about data visibility (domain) or
workflow participation (BP)?

**Trap 3: Forgetting the Two-Timestamp Model**

The exam tests whether you understand the difference between the "pending"
timestamp and the "active" timestamp. A common wrong answer is "the policy
became effective when it was saved." The correct answer is always "the policy
became effective when it was activated."

**Trap 4: Thinking Activation Is Per-Policy**

When you activate pending changes, you activate ALL pending changes across
the tenant, not just the one policy you edited. The exam may present a
scenario where an administrator activates changes and inadvertently pushes
another administrator's unreviewed edits live. This is a valid (and tested)
risk.

---
---

# MODULE 3 -- ADVANCED CONFIGURATION AND INHERITANCE

---

## 3.1 Deep Dive

### Inheritance Logic: Parent to Child Organisations

In Workday's supervisory organisation hierarchy, a constrained security role
assigned to a **parent** organisation is, by default, **inherited by all child
(subordinate) organisations**. This means:

- If User A is assigned the "HR Partner" role on the "Global HR" supervisory
  organisation, and "Global HR" has three subordinate organisations
  ("Americas HR," "EMEA HR," "APAC HR"), User A can access HR data for workers
  in ALL FOUR organisations (the parent plus the three children).

- If "Americas HR" has its own subordinate organisations ("US HR," "Canada HR"),
  User A's access extends to those as well. **Inheritance cascades all the way
  down** the hierarchy unless explicitly blocked.

- Inheritance applies to **constrained** roles only. Unconstrained roles already
  grant tenant-wide access, so inheritance is irrelevant for them.

**Rule of thumb:** Think of inheritance as water flowing downhill. A role
assigned at the top of a supervisory organisation tree flows down to every
branch and leaf unless you build a dam.

---

### How to Block Inheritance (Breaking the Chain)

Workday provides the ability to **block inheritance** at any level of the
supervisory organisation hierarchy. When inheritance is blocked on a child
organisation:

1. Navigate to the **subordinate organisation's** security settings.
2. Select the option to **"Block role inheritance for this organisation."**
3. Specify WHICH roles should be blocked. You can block all inherited roles
   or selectively block specific roles.
4. **Activate** the security policy changes (the same activation process
   from Module 2 applies here).

After blocking:

- The parent organisation's role holders **lose access** to the child
  organisation and all of the child's subordinates (the block cascades
  downward from the point of the block).
- The child organisation must have its **own** role assignments to maintain
  access for the relevant users.
- Blocking is **not retroactive** for business process events. If a business
  process was initiated before the block was applied, the original role
  holders may still have access to that specific event until it completes.

---

### Troubleshooting: Why a User Has Access They Should Not Have

The most common root cause is **aggregation of permissions**. Workday security
is **additive** (also called "union-based"). This means:

- If a user belongs to Security Group A (which grants View on Domain X) AND
  Security Group B (which grants Modify on Domain X), the user's effective
  access is **Modify** on Domain X (the higher of the two).

- There is **no "deny" rule** in Workday security. You cannot create a
  security policy that explicitly blocks access. You can only REMOVE a
  security group from a policy or REMOVE a user from a security group.

**Troubleshooting checklist for unintended access:**

```
1. IDENTIFY the domain or business process the user should
   not have access to.

2. RUN the report "View Security Groups for User" to list
   every security group the user belongs to.

3. For EACH security group listed, check whether it is
   included in the domain or BP security policy in question.

4. If a security group IS included, determine WHY the user
   is a member:
   a. User-Based group?   -> Check the manual membership list.
   b. Role-Based group?   -> Check which organisations the user
                             holds the role on. Check inheritance.
   c. Job-Based group?    -> Check the user's job profile, job
                             family, or job family group.
   d. Intersection group? -> Check the component groups.

5. RESOLVE by either:
   a. Removing the user from the security group, OR
   b. Removing the security group from the security policy, OR
   c. Blocking inheritance at the appropriate organisation level.

6. ACTIVATE the pending security changes.
```

**Key point:** Because Workday security is purely additive and has no deny
capability, the only way to restrict access is to ensure the user does NOT
belong to a security group that grants the unwanted access. Every security
group membership the user holds is evaluated, and the most permissive
combination wins.

---

## 3.2 Examiner's Trap

**Trap 1: Forgetting That Inheritance Flows Through ALL Levels**

Candidates sometimes assume that inheritance only applies to the immediate
child. It does not. If you assign a role at level 1, it flows to level 2,
level 3, level 4, and so on -- all the way to the leaf nodes. Blocking
inheritance at level 3 does NOT restore the block at level 4; the block at
level 3 already prevents the flow from reaching level 4 (and below).

**Trap 2: Assuming You Can "Deny" Access**

Workday has NO deny mechanism. If the exam presents an answer choice that
includes "create a deny rule" or "add an exclusion policy," it is incorrect.
The only way to remove access is to remove the membership or the policy
assignment itself.

**Trap 3: Overlooking Inactive or Pending Blocks**

If an administrator configured an inheritance block but forgot to activate
the pending security changes, the block is NOT in effect. The inheritance
continues to flow as before. Combined with Module 2's activation trap, this
is a favourite double-trap on the exam.

**Trap 4: Aggregation Across Multiple Organisations**

A user who holds the same constrained role on multiple organisations
(e.g., "HR Partner" on both "Americas HR" and "EMEA HR") has the **union**
of access from both contexts. If the exam describes a user whose access
seems broader than expected, check whether the user holds the role on
more than one organisation.

---
---

# MODULE 4 -- EXAMINER'S CORNER (SCENARIO-BASED QUESTIONS)

---

> **Instructions:** Treat each scenario as a timed exam question. Read the
> scenario, select your answer, and then review the technical reasoning to
> confirm or correct your understanding.

---

### Scenario 1: The Transferred Worker

**Question:**

A worker named Alex was transferred from the "Finance -- US" supervisory
organisation to the "Marketing -- EU" supervisory organisation last week.
However, Alex's former manager in Finance reports that Alex can still view
the Finance team's compensation data.

What is the MOST LIKELY reason Alex retained access?

**(A)** The transfer business process has not yet completed.
**(B)** Alex holds a user-based security group that grants view access to
compensation data.
**(C)** The compensation domain security policy was not activated after the
transfer.
**(D)** Inheritance from a parent organisation is granting Alex access to
Finance compensation data.

**Correct Answer: (B)**

**Technical Reasoning:**

When a worker transfers between supervisory organisations, constrained
role-based security group memberships automatically update because they are
tied to the organisational context. Alex would automatically lose any
constrained role-based access to Finance upon transfer completion. However,
**user-based security groups are manually maintained** and are NOT
automatically updated by organisational changes. If Alex was explicitly added
to a user-based security group that grants View access to the compensation
domain, that membership persists regardless of organisational transfers. The
administrator must manually remove Alex from the user-based group.

Option (A) is plausible but less likely because the question states the
transfer occurred "last week," implying the BP has completed. Option (C) is
incorrect because transfers do not require separate security policy
activation. Option (D) is incorrect because the inheritance would follow the
NEW organisation, not grant continued access to the old one.

---

### Scenario 2: The Invisible Report Field

**Question:**

An HR analyst runs a custom report that includes employee name, job title,
and annual salary. The analyst can see the employee name and job title but
the annual salary column is blank for all rows. The report developer confirms
the report is correctly configured. Other users can see all three fields.

What is the MOST LIKELY cause?

**(A)** The analyst's role-based security group does not include Modify access
to the compensation domain.
**(B)** The analyst's security groups do not include View access to the
compensation domain.
**(C)** The report has a filter that excludes salary data for the analyst's
security group.
**(D)** The compensation domain security policy has not been activated.

**Correct Answer: (B)**

**Technical Reasoning:**

Workday suppresses individual report fields when the user lacks
**domain-level View access** to the domain that governs those fields. The
report itself still renders, and fields in accessible domains are displayed.
The analyst can see name and job title (which are in domains she does have
View access to) but cannot see annual salary (which is in the compensation
domain she lacks View access to).

Option (A) is incorrect because Modify access is irrelevant for viewing
report data -- View is sufficient. Option (C) is incorrect because Workday
does not support security-group-based report filters in this manner. Option
(D) is possible but unlikely if "other users can see all three fields,"
meaning the policy IS active.

---

### Scenario 3: The Overpowered Integration

**Question:**

An Integration System User (ISU) for a benefits integration is extracting
data that includes employee Social Security numbers. The ISU was only
intended to extract benefits enrolment data -- NOT personally identifiable
information (PII) such as Social Security numbers.

What should the administrator do FIRST?

**(A)** Delete the ISU and create a new one with fewer permissions.
**(B)** Review the ISU's security group memberships and remove any group
that grants View access to the PII domain.
**(C)** Add a "deny" rule to the PII domain security policy for the ISU's
security group.
**(D)** Deactivate the benefits integration immediately.

**Correct Answer: (B)**

**Technical Reasoning:**

The ISU's access is governed by the security groups it belongs to, just like
any other user. The correct first step is to audit which security groups the
ISU is a member of and identify which group is granting View access to the
domain that contains Social Security numbers. Once identified, the
administrator should remove the ISU from that group (or remove the group from
the PII domain security policy) and then activate the pending changes.

Option (A) is unnecessarily destructive; modifying group membership is the
standard approach. Option (C) is impossible -- Workday has no deny mechanism.
Option (D) is an operational overreaction; the correct fix is a security
configuration change, not shutting down the integration.

---

### Scenario 4: The Double Activation Failure

**Question:**

An administrator made two changes on Monday:

1. Added a new security group to the "Hire" business process security policy
   with Initiate access.
2. Blocked inheritance of the "HR Partner" role on the
   "Engineering -- Germany" supervisory organisation.

On Tuesday, a recruiter in the new security group successfully initiates a
hire. However, the global HR Partner reports she can still see worker data
in Engineering -- Germany.

What went wrong?

**(A)** Only business process security policy changes were activated; the
inheritance block was not activated separately.
**(B)** The activation task was run twice, but the second activation reversed
the first.
**(C)** All pending changes were activated together, and both should be
in effect.
**(D)** Inheritance blocks cannot be applied to supervisory organisations
outside the administrator's own constrained scope.

**Correct Answer: (A)**

**Technical Reasoning:**

When the administrator ran "Activate Pending Security Policy Changes," **all
pending security policy changes** across the tenant are activated together.
However, **inheritance configuration changes** are saved and activated through
a DIFFERENT pathway -- they are part of the supervisory organisation's
configuration, not the security policy activation task. The administrator
must separately confirm the inheritance block within the organisation's
settings and then activate the relevant security changes. The recruiter's
access works because the BP policy change was included in the standard
activation. The HR Partner's inherited access persists because the
inheritance block follows a distinct activation path that was not completed.

Option (B) is incorrect; activations do not reverse each other. Option (C)
is incorrect because the inheritance block uses a different mechanism.
Option (D) is incorrect; inheritance blocks are not constrained by the
administrator's own scope in this manner.

---

### Scenario 5: The Intersection Oversight

**Question:**

A security architect creates an intersection security group called
"EMEA Benefits Admins" that requires membership in BOTH the "Benefits
Administrator" role-based security group AND the "EMEA Workers" job-based
security group. The architect assigns this intersection group View and
Modify access to the benefits enrolment domain.

A Benefits Administrator based in the US reports that she can also modify
benefits enrolment data, even though she does not belong to the
"EMEA Workers" group and therefore should not be a member of
"EMEA Benefits Admins."

What is the MOST LIKELY cause?

**(A)** Intersection groups do not actually restrict access; they only
expand it.
**(B)** The "Benefits Administrator" role-based security group is
ALSO directly assigned View/Modify access to the benefits enrolment
domain security policy, independent of the intersection group.
**(C)** The US-based administrator's job profile was incorrectly mapped to
the EMEA job-based group.
**(D)** The intersection group was not activated.

**Correct Answer: (B)**

**Technical Reasoning:**

Because Workday security is **additive**, the US-based Benefits Administrator
does not need to be in the intersection group to have access. If the
"Benefits Administrator" role-based security group is ALSO listed on the
benefits enrolment domain security policy with View/Modify permissions, then
**any** member of that role-based group gains access, regardless of whether
the intersection group exists. The intersection group adds a SECOND path to
access but does not REMOVE the first path. To achieve the architect's intent,
the "Benefits Administrator" role-based security group must be REMOVED from
the domain security policy, leaving ONLY the intersection group as the access
path.

Option (A) is incorrect; intersection groups DO restrict their own membership
(a user must be in both component groups). The problem is aggregation across
multiple security groups on the same policy. Option (C) is worth
investigating but the question states she does NOT belong to the EMEA group.
Option (D) could cause the intersection group to not work, but would not
explain why the US administrator HAS access -- it would explain only why
EMEA administrators LACK access.

---
---

# QUICK REFERENCE -- KEY TERMS FOR FINAL REVIEW

| Term | Definition |
|---|---|
| **OMS (Object Management System)** | Workday's unified data model; all securable items are objects within OMS |
| **Security Group** | A collection of users (or user criteria) used to grant access via security policies |
| **Constrained** | Access scoped to a specific organisational context (e.g., one supervisory org) |
| **Unconstrained** | Access applies to ALL instances across the entire tenant |
| **Domain Security Policy** | Controls View and/or Modify access to a security domain (data-level) |
| **Business Process Security Policy** | Controls Initiate, Review, and/or Approve actions within a workflow |
| **Functional Area** | An organisational grouping of related domains; does not grant access itself |
| **Policy Activation** | The mandatory step to make pending security changes effective tenant-wide |
| **Inheritance** | Constrained roles flow from parent to child supervisory organisations by default |
| **Aggregation** | A user's effective access is the UNION of all security group memberships; most permissive wins |
| **Intersection Security Group** | Requires membership in two or more component groups simultaneously |
| **Integration System User (ISU)** | A non-human account used by integrations; governed by the same security framework as human users |

---

# FINAL EXAM PREPARATION CHECKLIST

- [ ] I can list and compare all four security group types from memory.
- [ ] I can explain the difference between constrained and unconstrained access.
- [ ] I can describe how contextual security flows through supervisory organisations.
- [ ] I can explain the two permission levels of domain security policies.
- [ ] I can distinguish between Initiate, Review, and Approve in BP security.
- [ ] I can recite the policy activation critical path and explain what happens if activation is skipped.
- [ ] I understand that activation pushes ALL pending changes, not just one policy.
- [ ] I can explain parent-to-child inheritance and how to block it.
- [ ] I know that Workday security is additive (no deny rules exist).
- [ ] I can troubleshoot unintended access using the aggregation model.
- [ ] I can answer scenario questions about transfers, report suppression, ISU permissions, inheritance blocks, and intersection group aggregation.

---

*End of Exam Readiness Guide*
