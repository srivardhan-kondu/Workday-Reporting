# WORKDAY PRO HCM REPORTING CERTIFICATION -- EXAM QUESTION BANK

**Source:** Compiled from publicly available practice materials and community forums
**Exam Code:** Workday-Pro-HCM-Reporting
**Format:** 50 Multiple-Choice Questions | 120 Minutes | Proctored
**Print Format:** Black-and-White, A4-Optimised

---

> **Disclaimer:** These questions have been compiled from publicly shared
> practice materials, community discussions, and certification prep forums.
> They are intended for study purposes only. Always refer to official Workday
> Community documentation for the most current exam blueprint.

---

## TABLE OF CONTENTS

1. Reporting Fundamentals and Data Sources (Questions 1-10)
2. Calculated Fields (Questions 11-20)
3. Composite Reporting (Questions 21-28)
4. Trending Reports (Questions 29-35)
5. Report Security and Access (Questions 36-42)
6. Report Performance and Optimisation (Questions 43-50)

---
---

# SECTION 1: REPORTING FUNDAMENTALS AND DATA SOURCES

---

### Question 1

**The Chief Learning Officer wants you to build a report that lists all current
learning content and any information relating to ratings and popularity.
How should you find the relevant fields and data sources available to create
this report?**

(A) Search the Data Dictionary in Workday  
(B) Run the Business Object Details report  
(C) Navigate to the Learning functional area and browse fields manually  
(D) Contact Workday Support for a field listing  

**Correct Answer: (B)**

**Explanation:**
The **Business Object Details** report is Workday's built-in tool for discovering
available fields, relationships, and related business objects for any data source.
It displays all accessible fields that can be included in reporting. The Workday
documentation states: "The report data source provides the view into the primary
business object. This object gives you access to class report fields as well as
links to related business objects." The Business Object Details report is the
definitive resource for confirming which fields (e.g., Learning Content, Ratings,
Popularity) are accessible.

---

### Question 2

**A report writer needs to create a custom report. Which Workday tool should
they use to view which fields are available for a specific business object?**

(A) View Security for Securable Item report  
(B) Custom Report Data Source task  
(C) Business Object Details report  
(D) Report Performance Log  

**Correct Answer: (C)**

**Explanation:**
The **Business Object Details** report displays all available fields,
relationships, and related business objects for any given primary business object.
Option (A) relates to security auditing, not field discovery. Option (B) is for
creating reusable data source definitions. Option (D) is for performance analysis.

---

### Question 3

**What is the primary business object in a Workday report?**

(A) The security group assigned to the report  
(B) The data source that provides the view into the report's main entity  
(C) The calculated field that drives the report output  
(D) The prompt that filters the report at runtime  

**Correct Answer: (B)**

**Explanation:**
The **data source** provides the view into the primary business object. This
object gives access to class report fields and links to related business objects.
All reports are built on top of a primary business object which defines the
core entity being reported on (e.g., Workers, Positions, Organisations).

---

### Question 4

**An administrator wants to modify a standard (delivered) Workday report
to include additional fields. What is the correct approach?**

(A) Edit the standard report directly  
(B) Copy the standard report and then edit the copy  
(C) Delete the standard report and create a new custom report  
(D) Submit a request to Workday to modify the standard report  

**Correct Answer: (B)**

**Explanation:**
Standard (delivered) reports in Workday **cannot be directly edited**. To modify
them, you must **copy** the standard report, which creates a custom version, and
then edit the copy. This preserves the original delivered report for reference
and ensures future Workday updates do not overwrite your customisations.

---

### Question 5

**Which statement is TRUE about simple reports in Workday?**

(A) Simple reports can be exposed as web services  
(B) Simple reports cannot be used as web services  
(C) Simple reports support matrix grouping  
(D) Simple reports support sub-reports  

**Correct Answer: (B)**

**Explanation:**
**Simple reports cannot be used as web services.** Only **advanced reports** can
be exposed as web services for integration purposes. Simple reports are designed
for basic tabular display and lack the advanced features (web service exposure,
matrix grouping, sub-report support) available in advanced and matrix reports.

---

### Question 6

**A report allows sharing with "All users who have access to the report data
source." What does this mean?**

(A) All users in the tenant can run the report  
(B) Only users whose security groups grant access to the report's data source
domain can view and run the report  
(C) Only administrators can share the report  
(D) The report is public and does not require authentication  

**Correct Answer: (B)**

**Explanation:**
When a report is shared with "all users who have access to the report data
source," Workday enforces **domain security**. Only users whose security groups
include the appropriate permissions for the domain that secures the report's
data source will be able to see and run it. This is NOT tenant-wide access.

---

### Question 7

**What does a Custom Report Data Source (CRDS) provide?**

(A) A one-time data extraction for a single report  
(B) A reusable reporting foundation with defined fields, security, and
business logic that can be used across multiple custom reports  
(C) A log of all report executions  
(D) A tool for purging outdated report data  

**Correct Answer: (B)**

**Explanation:**
A **Custom Report Data Source (CRDS)** allows organisations to define a reusable
reporting foundation tailored to their specific needs. It provides flexibility
to define fields, security, and business logic centrally, improving consistency
and reducing effort across multiple custom reports. Multiple reports can
reference the same CRDS.

---

### Question 8

**A composite report allows reporting on which of the following?**

(A) Only one primary business object at a time  
(B) More than one primary business object  
(C) Only calculated fields, not raw data  
(D) Only security-related business objects  

**Correct Answer: (B)**

**Explanation:**
A **composite report** allows reporting on **more than one primary business
object**. It combines data from multiple sub-reports (which can have different
data sources) into a single cohesive output, providing a comprehensive view
of complex or hierarchical data.

---

### Question 9

**How does Workday ensure real-time data in reports?**

(A) Reports are cached for 24 hours  
(B) Reports pull from a separate data warehouse that syncs nightly  
(C) Workday uses its in-memory database (Object Management System) to
fetch current data upon execution  
(D) Reports use scheduled batch jobs to pre-compute results  

**Correct Answer: (C)**

**Explanation:**
Workday ensures real-time data through its **in-memory database** (Object
Management System -- OMS). Most reports fetch current data upon execution. Only
specific configurations such as caching or data snapshots (for trending) alter
this default real-time behaviour.

---

### Question 10

**Which data source type is recommended for optimised performance when
reporting on large volumes of data?**

(A) Standard data sources  
(B) Indexed data sources  
(C) Composite data sources  
(D) Trending data sources  

**Correct Answer: (B)**

**Explanation:**
**Indexed data sources** are specifically designed for faster retrieval and
better scalability. They are pre-optimised for reporting and queries on large
data volumes, making them the recommended choice when performance is a concern.

---
---

# SECTION 2: CALCULATED FIELDS

---

### Question 11

**You are creating a custom report to calculate the monthly bonus for each
worker in the sales department. The bonus is calculated as 10% of the total
sales for the month. What calculated field function would return the monthly
bonus for each worker?**

(A) Evaluate Expression  
(B) Arithmetic Calculation  
(C) Lookup Related Value  
(D) Sum Related Instances  

**Correct Answer: (B)**

**Explanation:**
The **Arithmetic Calculation** function is designed for mathematical operations
such as addition, subtraction, multiplication, and division. To calculate a
bonus as 10% of monthly sales, you multiply the sales field by 0.10. The Workday
documentation states: "Arithmetic Calculation -- Creates a numeric field using
mathematical operations performed on existing fields." **Evaluate Expression** is
for logical/Boolean conditions. **Lookup Related Value** retrieves fields from
related objects. **Sum Related Instances** aggregates multiple rows.

---

### Question 12

**An HR report requires a field that determines whether an employee is
classified as a manager. Which calculated field function is most appropriate?**

(A) Arithmetic Calculation  
(B) Evaluate Expression  
(C) Concatenate Text  
(D) Lookup Related Value  

**Correct Answer: (B)**

**Explanation:**
The **Evaluate Expression** function is used for **logical or Boolean
conditions** -- determining whether something is true or false. Checking if an
employee is a manager is a conditional check (Is Manager = True/False), making
Evaluate Expression the correct choice.

---

### Question 13

**You need to create a calculated field that returns a date 60 days after an
employee's Bonus Approval Date. Which function should you use?**

(A) Arithmetic Calculation  
(B) Increment or Decrement Date  
(C) Concatenate Text  
(D) Evaluate Expression  

**Correct Answer: (B)**

**Explanation:**
The **Increment or Decrement Date** function is specifically designed for date
arithmetic -- adding or subtracting days, months, or years from an existing
date field. To calculate a date 60 days after the Bonus Approval Date, you
would use this function with a +60 day increment.

---

### Question 14

**Which calculated field function would you use to combine an employee's
first name and last name into a single "Full Name" field?**

(A) Arithmetic Calculation  
(B) Evaluate Expression  
(C) Concatenate Text  
(D) Sum Related Instances  

**Correct Answer: (C)**

**Explanation:**
The **Concatenate Text** function combines multiple text strings into a single
output. To merge first name and last name (with a space separator) into a
"Full Name" field, Concatenate Text is the correct choice.

---

### Question 15

**A report needs to display the name of the supervisory organisation that
a position belongs to. The position is the primary business object. Which
calculated field function retrieves this data?**

(A) Evaluate Expression  
(B) Sum Related Instances  
(C) Lookup Related Value  
(D) Arithmetic Calculation  

**Correct Answer: (C)**

**Explanation:**
**Lookup Related Value** retrieves a field from a **related business object**.
Since the supervisory organisation name is on the Organisation object (which is
related to the Position object), Lookup Related Value traverses the relationship
and returns the organisation name.

---

### Question 16

**You need a calculated field that counts the total number of direct reports
for each manager. Which function is most appropriate?**

(A) Arithmetic Calculation  
(B) Lookup Related Value  
(C) Sum Related Instances  
(D) Evaluate Expression  

**Correct Answer: (C)**

**Explanation:**
**Sum Related Instances** aggregates data across multiple related records. To
count the total number of direct reports (multiple worker records) for each
manager, you sum/count across the related worker instances. Arithmetic
Calculation operates on single-row fields, not across multiple rows.

---

### Question 17

**What is the purpose of the "Lookup Hierarchy Rollup" function in
calculated fields?**

(A) It performs arithmetic on hierarchical data  
(B) It enables drill-down through hierarchical structures such as
supervisory organisations in matrix reports  
(C) It flattens a hierarchy into a single level  
(D) It restricts report access based on organisational hierarchy  

**Correct Answer: (B)**

**Explanation:**
The **Lookup Hierarchy Rollup** function enables **drillable hierarchies** in
matrix reports, showing metrics at each level of the organisational tree. Users
can expand results from the top supervisory organisation down to teams and
individual workers. This is the only function that creates drillable hierarchies.

---

### Question 18

**You are building a calculated field and need to convert a text value
to a number for use in arithmetic operations. Which approach is correct?**

(A) Use Arithmetic Calculation directly on the text field  
(B) Use a text-to-number conversion function before applying arithmetic  
(C) Use Concatenate Text to add the text to a number  
(D) Use Evaluate Expression  

**Correct Answer: (B)**

**Explanation:**
Text fields cannot be used directly in arithmetic operations. You must first
convert the text to a numeric value using a **text-to-number conversion function**
and then apply the Arithmetic Calculation. Using Arithmetic Calculation directly
on a text field would produce an error.

---

### Question 19

**Where can calculated fields be used in Workday? (Select the BEST answer)**

(A) Only in custom reports  
(B) In reports, integrations, and business processes  
(C) Only in integrations  
(D) Only in business processes  

**Correct Answer: (B)**

**Explanation:**
Calculated fields are versatile components that can be used across multiple areas
in Workday, including **reports, integrations, and business processes**. They are
not limited to a single functional area.

---

### Question 20

**A calculated field uses the "Evaluate Expression" function with the condition:
IF Worker is Terminated THEN "Inactive" ELSE "Active". What type of result
does this field return?**

(A) A numeric value  
(B) A date  
(C) A text/string value  
(D) A Boolean (true/false) value  

**Correct Answer: (C)**

**Explanation:**
Although **Evaluate Expression** evaluates a Boolean condition (Is Terminated?),
the THEN/ELSE branches in this example return text values ("Inactive" / "Active").
The result type is determined by what the expression returns, not by the
condition itself. In this case, the output is a **text/string value**.

---
---

# SECTION 3: COMPOSITE REPORTING

---

### Question 21

**You are building a composite report that uses two sub-reports with
different data sources. When running the composite report, users see
duplicate prompts. How should you resolve this?**

(A) Remove all prompts from the sub-reports  
(B) Configure a Prompt Set on the composite report in the Report Settings  
(C) Create a single shared data source for both sub-reports  
(D) Add a calculated field to suppress the duplicate prompt  

**Correct Answer: (B)**

**Explanation:**
When a composite report includes multiple sub-reports with their own prompts,
duplicate prompts can appear at runtime. The correct solution is to configure a
**Prompt Set** at the composite report level in Report Settings. The prompt set
consolidates prompts across sub-reports, eliminating redundancy and streamlining
the user experience. Removing all prompts (A) would eliminate necessary filtering.

---

### Question 22

**A sub-report's prompt is not appearing as available for mapping to the
composite report's prompt set. What is the MOST LIKELY cause?**

(A) The sub-report has no data  
(B) The prompt is configured with "Do Not Prompt at Runtime" or
"Use Value From Prompt Set"  
(C) The composite report has too many sub-reports  
(D) The sub-report's data source is incompatible  

**Correct Answer: (B)**

**Explanation:**
If a sub-report's prompt is configured with **"Do Not Prompt at Runtime"** or
**"Use Value From Prompt Set,"** it will not appear as available for mapping in
the composite report's prompt set. These settings explicitly control prompt
visibility and availability at the composite level.

---

### Question 23

**How do you add a matrix report as a component of a composite report?**

(A) Convert the matrix report to an advanced report first  
(B) Add the matrix report directly as a sub-report within the composite
report definition  
(C) Export the matrix report data and import it into the composite  
(D) Matrix reports cannot be used in composite reports  

**Correct Answer: (B)**

**Explanation:**
Matrix reports can be added **directly as sub-reports** within a composite
report definition. Each sub-report (including matrix reports) can have its own
data source. There is no need to convert the matrix report to another format.

---

### Question 24

**In a composite report, how is sorting typically determined?**

(A) At the composite report level globally  
(B) At the column level within each sub-report  
(C) By the prompt set configuration  
(D) Sorting is not available in composite reports  

**Correct Answer: (B)**

**Explanation:**
In composite reports, sorting is typically determined **at the column level**
within each sub-report. Each sub-report maintains its own column-level sort
configuration, which is preserved when rendered as part of the composite output.

---

### Question 25

**To ensure consistent grouping and summarisation across an entire composite
report, what must you do?**

(A) Apply a global filter at the composite level  
(B) Include the grouping field as "Detail Data" in ALL sub-reports  
(C) Use identical data sources for every sub-report  
(D) Configure a single calculated field that spans all sub-reports  

**Correct Answer: (B)**

**Explanation:**
To achieve consistent grouping across a composite report, you must include the
grouping field as **"Detail Data" in all sub-reports**. This ensures that the
same field is available for grouping and summarisation in every component,
producing a cohesive output.

---

### Question 26

**Which of the following can be configured within a composite report?
(Select the BEST answer)**

(A) Only data columns and prompts  
(B) Data columns, calculations, repeating column groups, column filters,
dynamic data rows, dynamic headers/footers, drill-down layout overrides,
and expansion hierarchies  
(C) Only data columns and security policies  
(D) Only drill-down layouts and headers  

**Correct Answer: (B)**

**Explanation:**
Composite reports offer extensive configuration options including **data columns,
calculations, repeating column groups, column filters, dynamic data rows,
dynamic headers and footers, drill-down layout overrides, and expansion
hierarchies**. This makes them among the most flexible report types in Workday.

---

### Question 27

**What is the primary advantage of using a composite report over running
multiple individual reports?**

(A) Faster execution time  
(B) Combined view of data from multiple business objects in a single output  
(C) Automatic security elevation  
(D) Reduced storage consumption  

**Correct Answer: (B)**

**Explanation:**
The primary advantage of composite reports is providing a **combined view of data
from multiple business objects in a single, cohesive output**. Rather than
running separate reports and manually correlating the results, a composite
report integrates everything into one user-friendly deliverable.

---

### Question 28

**You want to configure facet filters in a composite report for dynamic
filtering of results. Where do you configure this?**

(A) In the prompt set  
(B) In the composite report's filter configuration settings  
(C) In each sub-report individually  
(D) Facet filters are not available in composite reports  

**Correct Answer: (B)**

**Explanation:**
**Facet filters** for dynamic, interactive filtering of composite report results
are configured within the **composite report's filter configuration settings**.
They provide end users with an interactive way to narrow down results without
re-running the entire report.

---
---

# SECTION 4: TRENDING REPORTS

---

### Question 29

**You configured a trending report for an HR analyst that shows headcount
by country trends by quarter. The analyst wants to see the data by month
instead. How do you fulfil this requirement?**

(A) Edit the Column Grouping grid in the report  
(B) Edit the Group by Time Period field in the report definition  
(C) Add a runtime prompt for time period selection  
(D) Run the Maintain Trended Workers task to change the system setting  

**Correct Answer: (B)**

**Explanation:**
The **"Group by Time Period"** field in the report definition controls the
granularity of trending data display. Changing this from "Quarter" to "Month"
will display the data monthly without needing to regenerate or reconfigure
trending data. Editing the Column Grouping grid (A) changes layout, not
trending intervals. A prompt (C) does not change aggregation. The Maintain
Trended Workers task (D) changes system-wide setup, not individual reports.

---

### Question 30

**Which data source is specifically designed for trending reports that
track worker data over time?**

(A) All Workers  
(B) Trended Workers  
(C) Active Workers  
(D) Indexed Workers  

**Correct Answer: (B)**

**Explanation:**
The **Trended Workers** data source is specifically designed for trending reports.
It provides periodic snapshots of worker data at defined intervals, enabling
tracking of changes over time and variance calculations.

---

### Question 31

**A trending report using the Trended Workers data source needs to display
only snapshot data (not calculated variances). What is the most efficient
method to restrict the report?**

(A) Remove all variance columns manually  
(B) Add a report filter on the "Record Type" or "Snapshot" field  
(C) Create a separate report using a non-trending data source  
(D) Use a calculated field to hide variance rows  

**Correct Answer: (B)**

**Explanation:**
Adding a report filter on the **"Record Type" or "Snapshot" field** is the most
efficient method to restrict a trending report to snapshot data only. This
approach has minimal performance impact compared to creating separate reports
or using calculated fields for row suppression.

---

### Question 32

**A trending report is configured to track headcount changes. Which type
of data does the trending data source provide?**

(A) Only the most current data as of the report execution date  
(B) Snapshots at periodic intervals plus calculated variances  
(C) Only historical data with no current-period information  
(D) Aggregated annual totals only  

**Correct Answer: (B)**

**Explanation:**
Trending data sources provide **snapshots at periodic intervals** (daily, weekly,
monthly, etc.) plus **calculated variances** between periods. This combination
allows analysts to see both the state at each point in time and the change
between periods.

---

### Question 33

**The HR administrator is complaining about a trending report that runs
slowly. The report uses the Trended Workers data source and includes a
field from the related Worker business object. How can you improve
performance without altering the report requirements?**

(A) Add the required field to the Trended Workers data source  
(B) Create a calculated field to replace the related object field  
(C) Purge and re-create the trending data  
(D) Remove the field and document the limitation  

**Correct Answer: (A)**

**Explanation:**
Performance issues occur when trending reports pull fields from **related
business objects** instead of directly from the Trended Workers data source.
This requires Workday to perform additional joins at runtime, slowing execution.
Adding the required field **directly to the Trended Workers data source** ensures
the data is pre-joined and optimised for trending. The Workday documentation
states: "To improve performance, add commonly reported fields directly to the
Trended Workers object. Using related business object fields requires additional
joins and increases report runtime."

---

### Question 34

**What is the purpose of the "Maintain Trended Workers" task?**

(A) To configure individual trending report definitions  
(B) To manage the system-wide trending data collection schedule and
configuration  
(C) To delete all trending data  
(D) To adjust report security for trending reports  

**Correct Answer: (B)**

**Explanation:**
The **"Maintain Trended Workers"** task manages the **system-wide trending data
collection** schedule and configuration. It controls when and how trending
snapshots are captured across the tenant. It does not configure individual
report definitions.

---

### Question 35

**You want a trending report to display data from the last 12 months only.
Where do you configure this?**

(A) In the Maintain Trended Workers system task  
(B) In the report definition using the appropriate date range filter or
prompt  
(C) In the data source security policy  
(D) This cannot be configured; trending always shows all available data  

**Correct Answer: (B)**

**Explanation:**
The date range for a trending report is configured in the **report definition**
using date range filters or prompts. The Maintain Trended Workers task controls
data collection, not display scope. Individual report definitions control
what subset of the captured trending data is displayed to users.

---
---

# SECTION 5: REPORT SECURITY AND ACCESS

---

### Question 36

**Two users run the same custom report. User A can see all columns
(employee name, job title, and annual salary), but User B can see only
employee name and job title -- the salary column is blank. What is the
MOST LIKELY cause?**

(A) User B's report instance is corrupted  
(B) User B does not have access to the security domain that secures the
compensation/salary field  
(C) The report has a bug that suppresses data for some users  
(D) User B needs to refresh the browser cache  

**Correct Answer: (B)**

**Explanation:**
Workday enforces **domain security at the field level** within reports. If a
user lacks access to the security domain that governs a particular field, that
field is **suppressed** (appears blank) while the rest of the report renders
normally. User B cannot see the salary because her security groups do not
include View access to the compensation domain.

---

### Question 37

**What determines whether a user can view a specific report in Workday?**

(A) The user's job title  
(B) Whether the user belongs to a security group that has the necessary
permissions in the domain security policy securing the report's data source  
(C) The user's location  
(D) Whether the report was created by the same user  

**Correct Answer: (B)**

**Explanation:**
Report access is governed by **domain security policies**. A user must belong
to at least one security group that has been granted the necessary permissions
(View or Modify) in the domain security policy that secures the report's data
source. Job title, location, and report ownership are irrelevant to this
security check.

---

### Question 38

**Which report should an administrator run to analyse how access is
controlled for a specific Workday report or task?**

(A) Business Object Details  
(B) View Security for Securable Item  
(C) Report Performance Log  
(D) Audit Trail for Security Changes  

**Correct Answer: (B)**

**Explanation:**
The **"View Security for Securable Item"** report displays the security policies,
domains, and security groups that control access to a specific Workday element
(report, task, dashboard, etc.). It is the primary tool for security auditing
at the item level.

---

### Question 39

**A user needs unconstrained access to view all instances of employee
performance data across the entire tenant. What type of security group
membership is required?**

(A) A constrained role-based security group tied to one supervisory org  
(B) An unconstrained security group with View access to the performance
data domain  
(C) A job-based security group matching the user's job profile  
(D) An intersection security group combining two constrained groups  

**Correct Answer: (B)**

**Explanation:**
**Unconstrained** access means the user can view ALL instances of data across
the tenant, not limited to a specific organisational context. The user needs
membership in an **unconstrained security group** that has been granted View
access to the performance data domain. Constrained groups (A) limit access
to a specific org. Job-based groups (C) are tied to job profile criteria.
Intersection groups (D) narrow access further.

---

### Question 40

**Domain security policies control access to which of the following?**

(A) Business process workflow steps only  
(B) Data and reports (securable items within a domain)  
(C) Tenant-wide system settings only  
(D) User authentication and password policies  

**Correct Answer: (B)**

**Explanation:**
**Domain security policies** control access to **data and reports** -- the
securable items grouped within a domain. They determine View and Modify
permissions. **Business process security policies** (not domain security
policies) control workflow steps such as Initiate, Review, and Approve.

---

### Question 41

**What is the difference between domain security policies and business
process security policies?**

(A) They are the same; the terms are interchangeable  
(B) Domain security policies control data/report access (View, Modify);
business process security policies control transaction actions
(Initiate, Review, Approve)  
(C) Domain security policies control integrations; business process security
policies control reports  
(D) Domain security policies apply to administrators only; business process
security policies apply to all users  

**Correct Answer: (B)**

**Explanation:**
**Domain security policies** control access to data and reports with View and
Modify permissions. **Business process security policies** control participation
in workflow transactions with actions like Initiate, Review, and Approve.
They are distinct policy types that operate independently.

---

### Question 42

**To access items within a security domain, what is the minimum requirement
for a user?**

(A) The user must be a system administrator  
(B) The user must belong to at least one security group that has the
necessary permissions in that domain's security policy  
(C) The user must have a specific job title  
(D) The user must be assigned to a supervisory organisation  

**Correct Answer: (B)**

**Explanation:**
A user must belong to **at least one security group** that has been granted the
appropriate permissions (View and/or Modify) within the domain's security policy.
No specific job title, admin status, or organisational assignment is required
beyond the security group membership.

---
---

# SECTION 6: REPORT PERFORMANCE AND OPTIMISATION

---

### Question 43

**A Report Performance Log shows high "Top Level Filter Time" for a
custom report. What action is MOST LIKELY to improve performance?**

(A) Add more columns to the report  
(B) Replace report-level filters with built-in data source prompts  
(C) Convert the report from advanced to simple  
(D) Remove all calculated fields  

**Correct Answer: (B)**

**Explanation:**
High **"Top Level Filter Time"** indicates that the report spends excessive time
filtering data after retrieval. Using **built-in data source prompts** instead of
report-level filters improves performance because prompts restrict data **earlier
in the processing cycle** (at the data source level), reducing the volume of
data that needs to be filtered at runtime.

---

### Question 44

**What is the Report Performance Log used for?**

(A) Auditing security changes to reports  
(B) Tracking who has run a specific report  
(C) Analysing report execution performance metrics such as filter time,
row count, and total runtime  
(D) Configuring report sharing permissions  

**Correct Answer: (C)**

**Explanation:**
The **Report Performance Log** provides detailed performance metrics for report
executions, including Top Level Filter Time, total row count, and overall
runtime. It is the primary diagnostic tool for identifying and resolving
report performance issues.

---

### Question 45

**A custom report is slow because it includes fields from multiple related
business objects, requiring many joins at runtime. What is the recommended
approach to improve performance?**

(A) Remove the related fields and accept the limitation  
(B) Use a Custom Report Data Source (CRDS) or indexed data source that
pre-joins the required fields  
(C) Split the report into multiple smaller reports  
(D) Increase the report timeout setting  

**Correct Answer: (B)**

**Explanation:**
Using a **Custom Report Data Source (CRDS)** or **indexed data source** that
pre-joins the required fields eliminates the need for runtime joins, significantly
improving report performance. Pre-joined data sources are always preferred over
reports that traverse multiple object relationships at execution time.

---

### Question 46

**When should you use built-in data source prompts instead of report-level
filters?**

(A) When you want to display all data without restriction  
(B) When you want to improve report performance by restricting data earlier
in the processing cycle  
(C) When you want to apply security to the report  
(D) When you want to export the report to PDF  

**Correct Answer: (B)**

**Explanation:**
Built-in data source prompts restrict data at the **data source level**, which
is earlier in the processing pipeline than report-level filters. This means less
data is retrieved and processed, resulting in faster report execution. This is
particularly important for reports with large data volumes.

---

### Question 47

**An administrator wants to adjust a matrix report to display the top ten
hiring sources instead of the default three. Which setting should they
modify?**

(A) Number of Columns  
(B) Maximum Number of Rows  
(C) Report Timeout  
(D) Data Source Limit  

**Correct Answer: (B)**

**Explanation:**
The **"Maximum Number of Rows"** setting in the matrix report definition
controls how many rows (e.g., hiring sources) are displayed. Changing this value
from 3 to 10 will display the top ten hiring sources. This is a report
definition setting, not a system-wide configuration.

---

### Question 48

**A report uses the comparison type "Value specified in this filter" for
one of its filter conditions. What does this mean?**

(A) The filter value is dynamically determined at runtime by the user  
(B) The filter uses a fixed, hard-coded value that does not change between
executions  
(C) The filter references a calculated field  
(D) The filter is disabled  

**Correct Answer: (B)**

**Explanation:**
The **"Value specified in this filter"** comparison type applies a **fixed,
hard-coded value** to the filter. Unlike prompts (which allow user input at
runtime), this filter type always uses the same pre-defined value. It is useful
when you want consistent, unchanging criteria applied to every report execution.

---

### Question 49

**You need to filter a custom report to show only part-time employees.
Which approach is correct?**

(A) Add a prompt that asks the user to type "Part-Time" at runtime  
(B) Add a report filter on the employee type field with the comparison
"Value specified in this filter" set to "Part-Time"  
(C) Create a calculated field that returns only part-time workers  
(D) Change the report's data source to a part-time-only data source  

**Correct Answer: (B)**

**Explanation:**
Adding a **report filter** on the employee type field with the comparison
**"Value specified in this filter"** set to "Part-Time" ensures the report
consistently returns only part-time employees without requiring user input.
A prompt (A) would work but requires manual input each time. A calculated
field (C) adds unnecessary complexity. There is typically no "part-time-only"
data source (D).

---

### Question 50

**Which of the following is a valid strategy for improving the performance
of a Workday report? (Select ALL that apply)**

1. Use indexed data sources for large data volumes  
2. Replace report-level filters with built-in data source prompts  
3. Add commonly needed fields directly to the primary data source
   (e.g., Trended Workers) to avoid runtime joins  
4. Use Custom Report Data Sources (CRDS) for pre-joined fields  
5. Minimise the use of fields from related business objects  

**Correct Answer: All five (1, 2, 3, 4, and 5)**

**Explanation:**
All five strategies are **valid performance optimisation techniques** in
Workday reporting:

1. **Indexed data sources** are pre-optimised for large-volume queries.
2. **Data source prompts** restrict data earlier than filters.
3. **Adding fields to the primary data source** eliminates runtime joins.
4. **CRDS** centralises pre-joined data for reuse across reports.
5. **Minimising related object fields** reduces the number of joins.

---
---

# EXAM TOPIC WEIGHTAGE REFERENCE

| Exam Domain | Approximate Weightage | Questions in This Bank |
|---|---|---|
| Reporting Fundamentals / Data Sources | ~20% | Q1--Q10 |
| Calculated Fields | ~25% | Q11--Q20 |
| Composite Reporting | ~15% | Q21--Q28 |
| Trending Reports | ~15% | Q29--Q35 |
| Report Security and Access | ~15% | Q36--Q42 |
| Report Performance / Optimisation | ~10% | Q43--Q50 |

---

# QUICK-REFERENCE ANSWER KEY

| Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans |
|---|---|---|---|---|---|---|---|---|---|
| 1 | B | 11 | B | 21 | B | 31 | B | 41 | B |
| 2 | C | 12 | B | 22 | B | 32 | B | 42 | B |
| 3 | B | 13 | B | 23 | B | 33 | A | 43 | B |
| 4 | B | 14 | C | 24 | B | 34 | B | 44 | C |
| 5 | B | 15 | C | 25 | B | 35 | B | 45 | B |
| 6 | B | 16 | C | 26 | B | 36 | B | 46 | B |
| 7 | B | 17 | B | 27 | B | 37 | B | 47 | B |
| 8 | B | 18 | B | 28 | B | 38 | B | 48 | B |
| 9 | C | 19 | B | 29 | B | 39 | B | 49 | B |
| 10 | B | 20 | C | 30 | B | 40 | B | 50 | All |

---

*End of Exam Question Bank*
