# WORKDAY PRO HCM REPORTING -- COMPOSITE REPORTS EXAMINATION

## 60 Exam-Ready Questions with Answers and Explanations

**Exam Code:** Workday-Pro-HCM-Reporting
**Topic Focus:** Composite Reports (~15% of Exam Weightage)
**Print Format:** Black-and-White, A4-Optimised
**Difficulty:** EASY (Q1-20) | MEDIUM (Q21-42) | HARD (Q43-60)

---

> **Prepared by:** Senior Chief Examiner, Workday Reporting Certification
>
> These 60 questions cover every testable area of Composite Reports: definition
> and purpose, sub-reports, prompt sets, control fields, data columns, rows and
> cells, header/footer, drill-down, security, performance, and advanced
> scenario-based troubleshooting. Questions are grouped by difficulty.

---

## TABLE OF CONTENTS

- Section A: EASY -- Fundamentals (Q1-Q20)
- Section B: MEDIUM -- Configuration and Components (Q21-Q42)
- Section C: HARD -- Advanced Scenarios and Troubleshooting (Q43-Q60)

---
---

# SECTION A: EASY -- FUNDAMENTALS (Q1-Q20)

---

### Question 1 [EASY]

**What is a Composite Report in Workday?**

(A) A simple report based on a single data source
(B) A report that combines data from multiple sub-reports and data sources
into a single consolidated view
(C) A report that can only display matrix data
(D) A report exclusively used for financial reporting

**Correct Answer: (B)**

**Explanation:**
A **Composite Report** combines data from **multiple sub-reports and data
sources** into a single consolidated view. It acts as a container that
integrates different report types (Advanced, Matrix, Trending) to present a
unified output.

---

### Question 2 [EASY]

**When creating a new custom report, which report type must you select to
build a Composite Report?**

(A) Advanced
(B) Matrix
(C) Composite
(D) Simple

**Correct Answer: (C)**

**Explanation:**
To create a Composite Report, you select **"Composite"** as the report type
during the "Create Custom Report" process. This activates the composite
report designer with its unique tabs and configuration options.

---

### Question 3 [EASY]

**What types of reports can serve as sub-reports within a Composite Report?**

(A) Only Advanced reports
(B) Only Matrix reports
(C) Advanced, Matrix, and Trending reports
(D) Only Simple reports

**Correct Answer: (C)**

**Explanation:**
Composite Reports can include three types of sub-reports: **Advanced, Matrix,
and Trending** reports. Each type serves a different purpose -- Advanced for
dynamic data rows, Matrix for summarised/drill-down data, and Trending for
time-series analysis.

---

### Question 4 [EASY]

**Which sub-report type is recommended for including dynamic data rows
and maintaining sort orders?**

(A) Matrix Report
(B) Trending Report
(C) Advanced Report
(D) Simple Report

**Correct Answer: (C)**

**Explanation:**
**Advanced Reports** are recommended for including dynamic data rows and
maintaining sort orders within a composite report. They provide row-level
detail and flexible sorting that is preserved when displayed in the composite.

---

### Question 5 [EASY]

**Which sub-report type is recommended for summarising data or enabling
drill-down capabilities?**

(A) Advanced Report
(B) Matrix Report
(C) Trending Report
(D) Composite Report

**Correct Answer: (B)**

**Explanation:**
**Matrix Reports** are ideal for data summarisation and drill-down. They
present cross-tabulated summaries and allow users to click through to
detailed data, making them perfect for executive-level composite reports.

---

### Question 6 [EASY]

**Which sub-report type is recommended for analysing data trends over time?**

(A) Advanced Report
(B) Matrix Report
(C) Trending Report
(D) Simple Report

**Correct Answer: (C)**

**Explanation:**
**Trending Reports** are specifically designed for time-series analysis --
tracking data over monthly, quarterly, or annual periods. They use the
Trended Workers data source and are ideal for historical comparisons.

---

### Question 7 [EASY]

**What is a "Prompt Set" in a Composite Report?**

(A) A set of security rules for the report
(B) A common set of selection parameters defined at the composite report
level that can be passed to multiple sub-reports
(C) A list of all available data sources
(D) A formatting template for report output

**Correct Answer: (B)**

**Explanation:**
A **Prompt Set** defines common selection parameters at the composite report
level. When the user runs the composite report, these prompts collect values
(e.g., organisation, date range) and pass them to the relevant sub-reports,
eliminating duplicate prompts.

---

### Question 8 [EASY]

**What is the primary purpose of a Prompt Set?**

(A) To improve report security
(B) To eliminate duplicate prompts when multiple sub-reports share similar
selection parameters
(C) To add formatting to report output
(D) To restrict which users can run the report

**Correct Answer: (B)**

**Explanation:**
The primary purpose of a Prompt Set is to **eliminate duplicate prompts**.
Without a Prompt Set, if three sub-reports each require an "Organisation"
prompt, the user would be asked three separate times. The Prompt Set
consolidates these into a single prompt.

---

### Question 9 [EASY]

**What is a "Control Field" in a Composite Report?**

(A) A field that controls user access
(B) A field that links the composite report to its sub-reports based on
a common grouping parameter
(C) A field that calculates totals
(D) A field that formats the report output

**Correct Answer: (B)**

**Explanation:**
A **Control Field** is the linking mechanism between the composite report and
its sub-reports. It defines a common grouping parameter (often "Report Type")
that tells the composite report how to pull and organise data from each
sub-report.

---

### Question 10 [EASY]

**The Composite Report designer interface is often compared to which
application?**

(A) Microsoft Word
(B) Microsoft Excel / a spreadsheet
(C) Microsoft PowerPoint
(D) Microsoft Access

**Correct Answer: (B)**

**Explanation:**
The Composite Report designer is often compared to **Microsoft Excel** or a
spreadsheet. It provides a grid-based interface with rows, columns, and cells
where you can place data elements, calculations, and formatting.

---

### Question 11 [EASY]

**Can a Composite Report have ZERO sub-reports?**

(A) Yes -- it can display only static text and calculations
(B) No -- at least one sub-report is required for a functional composite report
(C) Yes -- but only if it uses calculated fields
(D) No -- at least three sub-reports are required

**Correct Answer: (B)**

**Explanation:**
A composite report requires **at least one sub-report** to function. Without
sub-reports, the composite report has no data source to pull from. The entire
value proposition of a composite report is combining sub-report data.

---

### Question 12 [EASY]

**Where do you configure the header and footer of a Composite Report?**

(A) In the sub-report definitions
(B) In the Header/Footer tab of the composite report definition
(C) In the security policy
(D) In the data source configuration

**Correct Answer: (B)**

**Explanation:**
Headers and footers are configured in the **Header/Footer tab** of the
composite report definition. This tab allows you to add titles, dates,
logos, and other contextual information that appears at the top and bottom
of the report output.

---

### Question 13 [EASY]

**How many tabs does a Composite Report definition typically have?**

(A) 3-4 tabs
(B) 5-6 tabs
(C) Approximately 15 tabs
(D) Only 1 tab

**Correct Answer: (C)**

**Explanation:**
A Composite Report definition has approximately **15 tabs**, including General,
Header/Footer, Column Headings, Prompts, Outcome, Share, Rows, Cells,
Security Domain Name, Sub Records, and Override Conditions. This reflects
the complexity and flexibility of composite reports.

---

### Question 14 [EASY]

**Which tab in a Composite Report definition shows all linked sub-reports,
their data sources, filters, and primary business items?**

(A) General tab
(B) Prompts tab
(C) Sub Records tab
(D) Outcome tab

**Correct Answer: (C)**

**Explanation:**
The **Sub Records tab** provides a comprehensive overview of all sub-reports
linked to the composite report, including their data sources, filters, primary
business items, and prompt configurations.

---

### Question 15 [EASY]

**What is the "Outcome" tab used for in a Composite Report?**

(A) Defining sub-reports
(B) Configuring how the report output is delivered (e.g., screen, file,
print)
(C) Setting security permissions
(D) Adding calculated fields

**Correct Answer: (B)**

**Explanation:**
The **Outcome tab** configures how the composite report output is delivered.
Options typically include on-screen viewing, file download (Excel, PDF), and
print. This determines the end-user experience when the report completes.

---

### Question 16 [EASY]

**What is the "Share" tab used for in a Composite Report?**

(A) Defining prompt sets
(B) Specifying which security groups or users can access the report
(C) Configuring data columns
(D) Adding filters

**Correct Answer: (B)**

**Explanation:**
The **Share tab** specifies which **security groups or users** can access and
run the composite report. Sharing must be configured for both the composite
report itself AND the underlying sub-reports.

---

### Question 17 [EASY]

**A Composite Report is shared with "HR Business Partners." Can those users
automatically see data from all sub-reports?**

(A) Yes -- sharing the composite automatically shares all sub-reports
(B) No -- each sub-report must also be shared with the same security
groups independently
(C) Yes -- but only if the sub-reports use the same data source
(D) No -- sub-reports cannot be shared at all

**Correct Answer: (B)**

**Explanation:**
Sharing the composite report does NOT automatically share its sub-reports.
**Each sub-report must be independently shared** with the appropriate security
groups. Users who can access the composite but not a sub-report will see
empty sections for that sub-report's data.

---

### Question 18 [EASY]

**What is a "Data" column type in a Composite Report?**

(A) A column that performs calculations
(B) A column that displays data pulled directly from a sub-report
(C) A column that links to external data sources
(D) A column that shows security information

**Correct Answer: (B)**

**Explanation:**
A **"Data" column** displays data pulled directly from a sub-report. It maps
a specific field from a sub-report to a column in the composite report's grid,
showing the raw data values.

---

### Question 19 [EASY]

**What is a "Calculation" column type in a Composite Report?**

(A) A column that shows raw data from a sub-report
(B) A column that performs mathematical operations on other columns
(e.g., sum, difference, percentage)
(C) A column that adds empty space
(D) A column that controls prompt behaviour

**Correct Answer: (B)**

**Explanation:**
A **"Calculation" column** performs mathematical operations on data from other
columns -- addition, subtraction, multiplication, division, percentage
calculations, etc. This allows you to compute derived metrics directly within
the composite report without modifying sub-reports.

---

### Question 20 [EASY]

**What is an "Empty Column" used for in a Composite Report?**

(A) To display error messages
(B) For visual formatting and spacing between data columns
(C) To store hidden data
(D) To trigger business processes

**Correct Answer: (B)**

**Explanation:**
**Empty Columns** are used purely for **formatting and visual spacing**. They
add whitespace between data columns to improve readability and create a
cleaner report layout.

---
---

# SECTION B: MEDIUM -- CONFIGURATION AND COMPONENTS (Q21-Q42)

---

### Question 21 [MEDIUM]

**When building a Composite Report, the Control Field is typically set
to which business object?**

(A) Worker
(B) Position
(C) Report Type
(D) Organisation

**Correct Answer: (C)**

**Explanation:**
The Control Field is typically set to **"Report Type"**, which serves as the
common grouping parameter linking all sub-reports. "Report Type" is a standard
Workday object that represents the report configuration and acts as the bridge
between the composite report and its sub-reports.

---

### Question 22 [MEDIUM]

**A Composite Report has two sub-reports that both require a "Cost Centre"
prompt. Without a Prompt Set, what happens when the user runs the composite
report?**

(A) The report fails with an error
(B) The user is prompted TWICE for "Cost Centre" -- once for each sub-report
(C) The system automatically consolidates the prompts
(D) The "Cost Centre" prompt is ignored

**Correct Answer: (C)**

**Explanation:**
Workday **automatically consolidates** duplicate prompts. If multiple
sub-reports use the same prompt (e.g., "Cost Centre"), Workday recognises the
duplication and presents a single consolidated prompt. The selected value is
applied consistently across all sub-reports. However, this automatic behaviour
can be explicitly managed using Prompt Sets for more complex scenarios.

---

### Question 23 [MEDIUM]

**When is a Prompt Set explicitly needed (not just automatic consolidation)?**

(A) When sub-reports use the same data source
(B) When sub-reports use DIFFERENT data sources but share similar selection
parameters, or when you need to set default values
(C) When the composite report has only one sub-report
(D) When the report has no filters

**Correct Answer: (B)**

**Explanation:**
Prompt Sets are explicitly needed when sub-reports use **different data sources**
but share similar parameters (Workday cannot auto-consolidate across different
data sources) or when you need to **establish default values** for prompts.
They are also useful when you want precise control over which sub-reports
receive which prompt values.

---

### Question 24 [MEDIUM]

**A sub-report has an "Organisation" prompt left open. What happens in the
composite report?**

(A) The prompt is hidden
(B) The open prompt automatically appears at the composite report level,
allowing the user to select the organisation when running the composite
(C) The sub-report fails
(D) The prompt defaults to "All Organisations"

**Correct Answer: (B)**

**Explanation:**
When a sub-report prompt is left **open** (not pre-filled), it **automatically
surfaces** at the composite report level. The user sees the prompt when they
run the composite report and can provide a value that is then passed to the
sub-report.

---

### Question 25 [MEDIUM]

**What is a "Lookup Field Value" column type used for in a Composite Report?**

(A) Performing arithmetic calculations
(B) Incorporating additional data based on lookup criteria from a related
business object
(C) Creating empty spacing columns
(D) Defining control fields

**Correct Answer: (B)**

**Explanation:**
A **"Lookup Field Value"** column incorporates additional data by performing
a lookup against a related business object based on specified criteria. This
allows the composite report to display data that is not directly available
in any of the sub-reports.

---

### Question 26 [MEDIUM]

**What is a "Repeating Group" column type used for?**

(A) To display static headers
(B) To establish repetition of values across a set of columns, creating
a repeating pattern for each instance of a group
(C) To hide duplicate data
(D) To merge cells

**Correct Answer: (B)**

**Explanation:**
**Repeating Groups** create a pattern of columns that repeats for each instance
of a grouping element. For example, if you group by "Month," a repeating group
with "Revenue" and "Expense" columns would display those two columns for
January, February, March, etc.

---

### Question 27 [MEDIUM]

**Best practice states that each Composite Report should have its own
dedicated sub-reports. Why?**

(A) Workday enforces this as a requirement
(B) Sharing sub-reports across multiple composite reports can lead to
performance issues and unintended data changes if the original sub-report
is modified
(C) Sub-reports can only belong to one composite
(D) For security compliance reasons only

**Correct Answer: (B)**

**Explanation:**
Using **dedicated sub-reports** prevents two problems: (1) **Performance
degradation** when a sub-report includes fields needed by one composite but
not another, and (2) **Unintended changes** when someone modifies a shared
sub-report, unknowingly affecting another composite report. Dedicated
sub-reports provide isolation.

---

### Question 28 [MEDIUM]

**How can you get a comprehensive "one-stop-shop" view of all elements
in a Composite Report?**

(A) Export the report to Excel
(B) Use the "Print" action under Related Actions > Custom Report > Print
(C) View the General tab only
(D) Run the report with no prompts

**Correct Answer: (B)**

**Explanation:**
Using **Related Actions > Custom Report > Print** generates a comprehensive
overview of the composite report's configuration. This "one-stop-shop" view
includes all tabs: General, Header/Footer, Column Headings, Prompts, Outcome,
Share, Rows, Cells, Security Domain Name, Sub Records, and Override Conditions.

---

### Question 29 [MEDIUM]

**Which tab lists all prompts active on the composite report (distinct from
sub-report prompts)?**

(A) General tab
(B) Prompts tab
(C) Sub Records tab
(D) Rows tab

**Correct Answer: (B)**

**Explanation:**
The **Prompts tab** lists all prompts that are active specifically on the
composite report itself. This is distinct from prompts defined within
individual sub-reports. It helps you audit and manage the composite-level
prompt configuration.

---

### Question 30 [MEDIUM]

**What does the "Rows" tab in a Composite Report configure?**

(A) Report security
(B) The row structure of the report grid, including data rows, calculation
rows, section headers, and row-level filters
(C) Sub-report definitions
(D) Prompt sets only

**Correct Answer: (B)**

**Explanation:**
The **Rows tab** configures the complete row structure: data rows (pulling
from sub-reports), calculation rows (computing derived values), section
headers (for visual grouping), and row-level filters. It defines what
appears on each row of the composite output.

---

### Question 31 [MEDIUM]

**What does the "Cells" tab in a Composite Report configure?**

(A) Only the font colour of cells
(B) Individual cell configurations including data references, calculations,
formatting overrides, and conditional formatting
(C) Sub-report selections only
(D) Security domain assignments

**Correct Answer: (B)**

**Explanation:**
The **Cells tab** provides granular control over individual cells in the
composite grid. You can configure data references (which sub-report field
populates the cell), calculations, formatting overrides (bold, colour), and
conditional formatting rules.

---

### Question 32 [MEDIUM]

**A Composite Report needs to display headcount, turnover rate, and open
positions. These come from three different data sources. How should you
structure the sub-reports?**

(A) Use a single Advanced report with all three data sources
(B) Create three separate sub-reports, each using the appropriate data
source, and combine them in the composite
(C) Use only one data source and ignore the other two
(D) Create a single Trending report for all three metrics

**Correct Answer: (B)**

**Explanation:**
Create **three separate sub-reports**, each using its appropriate data source:
one for headcount, one for turnover, and one for open positions. The composite
report then combines these three sub-reports into a unified view. This is the
fundamental purpose of composite reporting.

---

### Question 33 [MEDIUM]

**A required prompt on a sub-report is not marked with an asterisk in the
composite report. What is the MOST LIKELY cause?**

(A) The prompt is optional
(B) For custom prompts, the "Required" checkbox must be explicitly checked
on the Prompts tab; Workday only automatically marks Workday-delivered
data source requirements
(C) The composite report overrides all prompt requirements
(D) Required prompts do not display asterisks in composite reports

**Correct Answer: (B)**

**Explanation:**
Workday automatically marks **delivered data source requirements** with an
asterisk. For **custom prompts**, you must explicitly check the **"Required"
checkbox** on the Prompts tab. If it is not checked, the prompt appears as
optional even if the sub-report expects a value.

---

### Question 34 [MEDIUM]

**How do you convert a sub-report filter into a composite-level prompt?**

(A) Delete the filter and recreate it as a new prompt
(B) On the sub-report filter, select "Prompt the user for the value"
instead of providing a default value; the prompt then surfaces at the
composite level
(C) Filters cannot become prompts
(D) Add the filter to the Prompt Set

**Correct Answer: (B)**

**Explanation:**
When configuring a filter in a sub-report, you can choose **"Prompt the user
for the value"** (for required prompts) or **"Prompt the user and ignore if
blank"** (for optional prompts). This surfaces the filter as a prompt at the
composite report level, letting the user provide the value at runtime.

---

### Question 35 [MEDIUM]

**A Composite Report has an Advanced sub-report and a Matrix sub-report.
The Advanced sub-report shows detailed worker records. The Matrix sub-report
summarises the same data with drill-down. Is this a valid configuration?**

(A) No -- you cannot mix sub-report types
(B) Yes -- combining Advanced (detail) and Matrix (summary with drill-down)
sub-reports is a common and valid composite report pattern
(C) No -- Matrix reports cannot be sub-reports
(D) Yes, but only if they use the same data source

**Correct Answer: (B)**

**Explanation:**
Combining an Advanced sub-report (for detail) with a Matrix sub-report (for
summary and drill-down) is a **common and valid pattern**. This gives users
both a high-level summary view and detailed row-level data in a single
composite output.

---

### Question 36 [MEDIUM]

**What is the "Override Conditions" tab used for in a Composite Report?**

(A) Overriding security policies
(B) Defining conditional logic that alters the report's display behaviour
based on runtime conditions (e.g., hiding rows if values are zero)
(C) Overriding sub-report filters
(D) Overriding prompt default values

**Correct Answer: (B)**

**Explanation:**
The **Override Conditions tab** allows you to define conditional display logic.
For example, you can hide a row if its value is zero, change formatting based
on thresholds, or alter cell content based on runtime conditions. This provides
dynamic report behaviour.

---

### Question 37 [MEDIUM]

**A Composite Report is configured with three sub-reports from different data
sources. The user runs the report and sees data from only two of the three
sub-reports. The third section is blank. What should you check FIRST?**

(A) The composite report's calculated fields
(B) Whether the user has security access (domain security) to the third
sub-report's data source and fields
(C) The report's header and footer configuration
(D) The output format setting

**Correct Answer: (B)**

**Explanation:**
The first check should be **security access**. If the user lacks access to the
**security domain** securing the third sub-report's data source or fields,
that section will display as blank. The composite report itself runs, but the
secured sub-report returns no data for that user.

---

### Question 38 [MEDIUM]

**Can a Composite Report include drill-to-report links?**

(A) No -- drill-down is not available in composite reports
(B) Yes -- you can configure drill-to-report links within composite report
columns, allowing users to click through to detailed reports
(C) Only if all sub-reports are Matrix type
(D) Only through calculated fields

**Correct Answer: (B)**

**Explanation:**
Composite reports support **drill-to-report links** that allow users to click
on a value and navigate to a more detailed report. This is configured within
the column definitions and enhances the interactive experience of the
composite report.

---

### Question 39 [MEDIUM]

**What is the "Column Headings" tab used for?**

(A) Defining calculated fields
(B) Listing column heading rows and their filter/sort options, controlling
how column headers are displayed and organised
(C) Adding sub-reports
(D) Configuring security

**Correct Answer: (B)**

**Explanation:**
The **Column Headings tab** configures how column headers are displayed,
including heading text, grouping, filter options, and sort behaviour. It
controls the visual presentation of the column structure.

---

### Question 40 [MEDIUM]

**A Composite Report needs to display data from multiple time periods
side by side (e.g., Q1 vs Q2 vs Q3). Which sub-report type is BEST for this?**

(A) Advanced Report with three separate queries
(B) Trending Report configured with quarterly grouping
(C) Matrix Report with no groupings
(D) Simple Report

**Correct Answer: (B)**

**Explanation:**
A **Trending Report** with quarterly grouping natively organises data by time
period and displays Q1, Q2, and Q3 side by side. This is its designed purpose
and avoids the complexity of building three separate Advanced reports.

---

### Question 41 [MEDIUM]

**What is the "Security Domain Name" tab used for in a Composite Report?**

(A) Assigning the report to a security domain that controls which users
can access it
(B) Listing all security groups in the tenant
(C) Configuring row-level security
(D) Defining calculated field security

**Correct Answer: (A)**

**Explanation:**
The **Security Domain Name tab** assigns the composite report to a specific
**security domain**. Users must have access to this domain (via their security
group memberships) to be able to run the report. This is a core security
control.

---

### Question 42 [MEDIUM]

**A Composite Report has a Prompt Set with "Organisation" and "Effective
Date." Sub-Report A uses both prompts. Sub-Report B only uses
"Organisation." What happens to the "Effective Date" prompt for Sub-Report B?**

(A) Sub-Report B fails because it does not use "Effective Date"
(B) The "Effective Date" prompt value is passed to Sub-Report B but
ignored because Sub-Report B has no corresponding filter for it
(C) The entire composite report fails
(D) Sub-Report B automatically creates a new "Effective Date" filter

**Correct Answer: (B)**

**Explanation:**
Workday passes the Prompt Set values to all sub-reports, but if a sub-report
has **no corresponding filter or prompt** for a particular value, it simply
**ignores** it. Sub-Report B processes only the "Organisation" value and
disregards "Effective Date" without error.

---
---

# SECTION C: HARD -- ADVANCED SCENARIOS AND TROUBLESHOOTING (Q43-Q60)

---

### Question 43 [HARD]

**Scenario: A report writer builds a Composite Report with Sub-Report A
(Advanced) and Sub-Report B (Matrix). Sub-Report A is shared with "HR
Partners" and "HR Admins." Sub-Report B is shared with "HR Admins" only.
The composite report is shared with "HR Partners." What does an HR Partner
user see when they run the composite report?**

(A) They see data from both Sub-Report A and Sub-Report B
(B) They see data from Sub-Report A only; Sub-Report B's section is blank
because they lack access to it
(C) The report fails with a security error
(D) They see Sub-Report B only

**Correct Answer: (B)**

**Explanation:**
The HR Partner user has access to the composite report and Sub-Report A, but
NOT Sub-Report B. Workday does not fail the entire report -- it renders
Sub-Report A's data and displays **blank/empty** for Sub-Report B's section.
This is by design: composite report sections degrade gracefully based on
security. The fix is to share Sub-Report B with "HR Partners."

---

### Question 44 [HARD]

**Scenario: A Composite Report has three sub-reports all using the "Workers
for HCM Reporting" data source. The user reports seeing duplicate prompts
for "Supervisory Organisation" when running the report. However, Workday
should auto-consolidate identical prompts. What is the MOST LIKELY cause?**

(A) Workday has a bug
(B) The prompts in the different sub-reports are configured with slightly
different labels, field references, or filter conditions, preventing Workday
from recognising them as identical
(C) Duplicate prompts are always expected
(D) The data source does not support prompt consolidation

**Correct Answer: (B)**

**Explanation:**
Workday auto-consolidates prompts that are **identical** -- same field
reference, same label, same conditions. If sub-reports use **slightly different
configurations** (e.g., different default values, different filter conditions,
or different field paths even if they ultimately reference the same field),
Workday treats them as distinct prompts. The fix is to standardise the prompt
configuration across sub-reports or use a **Prompt Set** to explicitly
consolidate them.

---

### Question 45 [HARD]

**Scenario: A Composite Report includes a Calculation column that divides
"Revenue" (from Sub-Report A) by "Headcount" (from Sub-Report B). For one
department, headcount is zero. What happens?**

(A) The report displays zero
(B) The cell displays an error, NULL, or blank depending on configuration;
this is a division-by-zero scenario
(C) The report fails entirely
(D) The value defaults to 1.0

**Correct Answer: (B)**

**Explanation:**
Division by zero in a Calculation column produces **NULL/blank or an error**
in the affected cell. The rest of the report continues to render normally.
Best practice is to add conditional logic or override conditions to handle
zero-headcount scenarios (e.g., display "N/A" instead of computing the
division).

---

### Question 46 [HARD]

**Scenario: A Composite Report has a sub-report that is also used as a
standalone report by another team. A colleague modifies the standalone
sub-report by adding new filters. The Composite Report now shows different
data than expected. What happened?**

(A) The composite report's cache is stale
(B) Because the sub-report is shared between the composite and standalone
usage, the filter changes to the standalone sub-report affected the
composite report's data as well
(C) The data source was changed
(D) A security policy was updated

**Correct Answer: (B)**

**Explanation:**
This is the exact scenario that the **"dedicated sub-reports"** best practice
prevents. When a sub-report is shared across multiple uses, modifications
made for one purpose (standalone usage) affect all other uses (composite
report). The fix is to create a dedicated copy of the sub-report for the
composite report, isolating it from external changes.

---

### Question 47 [HARD]

**Scenario: A Composite Report with 5 sub-reports runs very slowly
(over 10 minutes). The report performance log shows that Sub-Report 3
takes 8 minutes. What is your recommended troubleshooting approach?**

(A) Delete all sub-reports and rebuild from scratch
(B) Investigate Sub-Report 3 independently: check its data source
efficiency, filter configuration, number of fields, calculated field
complexity, and whether it includes unnecessary fields not used by the
composite
(C) Switch Sub-Report 3 from Advanced to Matrix type
(D) Increase the system timeout limit

**Correct Answer: (B)**

**Explanation:**
Focus on **Sub-Report 3** since it is the bottleneck. Investigate: (1) Is the
data source efficient and indexed? (2) Are filters applied early and
selectively? (3) Are there excessive or complex calculated fields? (4) Does
the sub-report include fields not needed by the composite? Optimising the
slowest sub-report has the greatest impact on overall composite performance.

---

### Question 48 [HARD]

**Scenario: A Composite Report needs to display employee data alongside
their compensation AND benefits information. Compensation uses the
"Compensation" data source. Benefits uses the "Benefits" data source.
Employee demographics use the "Workers" data source. How should this be
structured?**

(A) Create one sub-report with all three data sources
(B) Create three sub-reports (one per data source) and combine them
in the composite report, using the worker as the common linking element
(C) Use only the Workers data source and ignore compensation and benefits
(D) Create a single matrix report

**Correct Answer: (B)**

**Explanation:**
Create **three dedicated sub-reports**, each using its specialised data source:
one for demographics (Workers), one for compensation (Compensation), and one
for benefits (Benefits). The composite report combines them, with the worker
serving as the common linking element across all three. This is the textbook
use case for composite reports.

---

### Question 49 [HARD]

**Scenario: An analyst configures a Composite Report with a Prompt Set
that includes "Organisation" and "Date Range." One sub-report uses a
different field path for "Organisation" than the other two sub-reports.
The Prompt Set value is not being passed correctly to that sub-report.
Why?**

(A) Prompt Sets do not support "Organisation" prompts
(B) The Prompt Set maps its prompt value to a specific field path; if a
sub-report's "Organisation" field uses a different path than the one
configured in the Prompt Set, the mapping fails
(C) The sub-report is corrupted
(D) Prompt Sets can only pass values to two sub-reports

**Correct Answer: (B)**

**Explanation:**
Prompt Sets map values to **specific field paths** on business objects. If a
sub-report references "Organisation" via a different relationship path (e.g.,
through Position > Organisation vs. directly through Worker > Organisation),
the Prompt Set mapping does not match. The fix is to ensure the field path
in the sub-report aligns with the Prompt Set configuration, or to configure
separate prompt mappings for different paths.

---

### Question 50 [HARD]

**Scenario: A Composite Report shows "N/A" in several cells where data
is expected. The sub-reports run correctly when executed independently.
What should you investigate?**

(A) The composite report's formatting settings
(B) The cell-to-sub-report field mapping in the Cells tab -- incorrect
references produce N/A or blank; also verify the Control Field and row-
to-sub-report linkage is correct
(C) The data source indexing
(D) The Workday tenant configuration

**Correct Answer: (B)**

**Explanation:**
When sub-reports work independently but cells show "N/A" in the composite,
the issue is typically in the **cell-to-sub-report mapping**. Check: (1) Does
each cell correctly reference the right sub-report field? (2) Is the Control
Field properly configured? (3) Is the row correctly linked to the appropriate
sub-report? Misconfigurations at the composite level produce N/A even when
the underlying data exists.

---

### Question 51 [HARD]

**Scenario: A financial controller needs a Composite Report that acts as
a Profit & Loss statement. It should show Revenue (from one data source),
Cost of Goods Sold (from another), and calculate Gross Profit (Revenue
minus COGS). Where is the Gross Profit calculation defined?**

(A) In a sub-report
(B) As a Calculation row/column in the composite report itself, referencing
the Revenue and COGS data columns
(C) In a separate calculated field
(D) In the data source

**Correct Answer: (B)**

**Explanation:**
Gross Profit (Revenue - COGS) is a **cross-sub-report calculation** that
can only be performed at the **composite report level**. It is defined as a
**Calculation row or column** in the composite report, referencing the Revenue
value from Sub-Report A and the COGS value from Sub-Report B. Neither
sub-report can compute this because they don't have access to each other's
data.

---

### Question 52 [HARD]

**Scenario: A Composite Report has conditional column outlining configured.
After adding a new cell with an unexpected conditional value, the column
outlining stops working. What should you try?**

(A) Rebuild the entire composite report
(B) Delete and recreate the affected repeating column groups or associated
rows to reset the conditional behaviour
(C) Change the report type to Advanced
(D) Remove all sub-reports

**Correct Answer: (B)**

**Explanation:**
Unexpected conditional values on cells can interfere with column outlining
behaviour. The fix is to **delete and recreate** the affected repeating column
groups or associated rows to reset the conditional logic. This clears the
conflicting configuration without rebuilding the entire report.

---

### Question 53 [HARD]

**Scenario: A Composite Report needs to show year-over-year headcount
comparison (Current Year vs. Prior Year) with variance. You have 24 months
of trending data. What is the MOST efficient approach?**

(A) Create two separate Advanced sub-reports with manual date filters
(B) Create a single Trending sub-report with "Group by Time Period = Annual"
and include it in the composite report; the trending report natively handles
the year-over-year comparison with built-in variance
(C) Create two composite reports and compare them manually
(D) Use a calculated field to compute variance in the composite

**Correct Answer: (B)**

**Explanation:**
A **single Trending sub-report** with annual grouping natively displays
year-over-year data with built-in variance calculations. This is far more
efficient than building two separate reports with manual date filters. The
composite report then simply integrates this trending sub-report alongside
other sub-reports for a complete view.

---

### Question 54 [HARD]

**Scenario: A Composite Report in production has 8 sub-reports and runs
in 25 minutes (approaching the 30-minute foreground limit). What are
TWO recommended actions?**

(A) Accept the performance and hope it does not degrade further
(B) Schedule the report as a background process (6-hour limit) AND
optimise the slowest sub-reports by reviewing data sources, filters,
and calculated field complexity
(C) Delete 4 sub-reports to reduce execution time
(D) Convert the composite to a matrix report

**Correct Answer: (B)**

**Explanation:**
Two actions: (1) **Schedule as a background process** to buy time with the
6-hour limit, and (2) **Optimise the slowest sub-reports** (identified via the
performance log) by improving data sources, tightening filters, and reducing
calculated field complexity. This addresses both the immediate timeout risk
and the root cause.

---

### Question 55 [HARD]

**Scenario: A Composite Report needs to display a financial summary where
some rows should only appear if their value exceeds a threshold (e.g.,
hide expense lines under $1,000). How is this configured?**

(A) By deleting rows with small values from the sub-report
(B) Using the Override Conditions tab to add a conditional rule that hides
rows when the value is below the threshold
(C) By adding a filter to the sub-report (which only filters source data,
not calculated composite rows)
(D) This is not possible in Workday

**Correct Answer: (B)**

**Explanation:**
The **Override Conditions tab** supports conditional display logic. You
configure a rule such as: IF value < 1000 THEN hide this row. This dynamically
controls row visibility at runtime without affecting the sub-report data.
Sub-report filters (C) would work for filtering source data but not for
composite-level calculation rows.

---

### Question 56 [HARD]

**Scenario: A CHRO requests a composite dashboard showing: (1) Headcount
trend by month, (2) Turnover rate by quarter, (3) Top 10 open positions,
and (4) Employee demographics summary. How should the sub-reports be
structured?**

(A) One single sub-report covering everything
(B) Four sub-reports: (1) Trending Report for monthly headcount, (2) Trending
Report for quarterly turnover, (3) Advanced Report for open positions with
sort/limit, (4) Matrix Report for demographics summary
(C) Two sub-reports only
(D) Use a worklet instead

**Correct Answer: (B)**

**Explanation:**
Each view requires a different report type and data source:
1. **Trending Report** -- monthly headcount snapshots
2. **Trending Report** -- quarterly turnover rate with variance
3. **Advanced Report** -- detailed list of open positions (sorted/limited to 10)
4. **Matrix Report** -- demographics summary with drill-down

This four-sub-report composite provides the complete dashboard the CHRO needs.

---

### Question 57 [HARD]

**Scenario: A Composite Report was running correctly. After a Workday
update, users report that a previously visible Calculation column now
shows blank values. The formula is: "Column A / Column B." Column A
and Column B still show correct values. What should you check?**

(A) Whether the Workday update changed the formula syntax
(B) Whether the cell references in the Calculation column are still
valid -- Workday updates can occasionally reset or invalidate cell
references in composite calculations; re-verify and reconfigure the
cell references
(C) Whether the sub-reports were deleted
(D) Whether the security policy was changed

**Correct Answer: (B)**

**Explanation:**
Workday updates can occasionally affect **cell references** in composite
report calculations. If the formula syntax or cell reference structure
changed between versions, existing calculations may become invalid and
display blanks. The fix is to **re-verify and reconfigure** the cell
references in the Calculation column to ensure they point to the correct
source cells.

---

### Question 58 [HARD]

**Scenario: You need to add a new sub-report to an existing Composite
Report. After adding it, users report that the composite report now
takes twice as long to run. The new sub-report runs in under 30 seconds
independently. What could cause this?**

(A) The composite report has a hard limit on sub-reports
(B) The new sub-report may include fields, security checks, or data
source joins that interact poorly with the composite's existing
configuration; additionally, the sub-report may include many fields
not needed by the composite, adding unnecessary processing overhead
(C) Adding sub-reports always doubles execution time
(D) The report needs to be deleted and recreated

**Correct Answer: (B)**

**Explanation:**
A sub-report that runs quickly independently may interact poorly with the
composite context. Common causes: (1) The sub-report includes **many fields
not needed** by the composite (all fields are still processed and security-
checked). (2) The sub-report's data source requires **joins** that conflict
with other sub-reports' processing. (3) The additional **security checks**
across more fields slow overall execution. The fix is to create a
**dedicated, lean sub-report** with only the fields the composite needs.

---

### Question 59 [HARD]

**Scenario: A Composite Report uses Prompt Set A with "Company" and "Date."
A new requirement asks for Sub-Report C to be added, which needs a
"Location" prompt not relevant to the other sub-reports. How should you
configure the prompts?**

(A) Add "Location" to Prompt Set A (forcing all users to select Location
even though other sub-reports do not need it)
(B) Leave the "Location" prompt as an open prompt on Sub-Report C; it
will automatically surface at the composite level without affecting the
other sub-reports or the existing Prompt Set
(C) Create a second composite report for Sub-Report C
(D) Remove the Prompt Set entirely

**Correct Answer: (B)**

**Explanation:**
The cleanest approach is to leave "Location" as an **open prompt on Sub-Report
C** only. It automatically appears at the composite level alongside the Prompt
Set prompts. Users see "Company" and "Date" (from the Prompt Set) plus
"Location" (from Sub-Report C's open prompt). The other sub-reports are
unaffected because they have no "Location" filter.

---

### Question 60 [HARD]

**Scenario: An auditor notices that a Composite Report shows different
headcount figures than the HR system's official count. After investigation,
you discover the composite uses three sub-reports that each count
workers independently. Some workers appear in multiple sub-reports due
to overlapping data source criteria. What is the root cause and fix?**

(A) The data is corrupted
(B) The root cause is overlapping data source criteria across sub-reports,
causing the same workers to be counted multiple times. The fix is to ensure
each sub-report uses mutually exclusive criteria (non-overlapping filters)
or to use a single authoritative sub-report for headcount and reference
its values in the composite calculations
(C) The composite calculations are wrong
(D) Security is filtering out some workers

**Correct Answer: (B)**

**Explanation:**
When multiple sub-reports count workers independently using overlapping
criteria, the same worker can be counted 2-3 times across sub-reports,
inflating the composite total. Two fixes: (1) Ensure sub-reports use
**mutually exclusive filters** so no worker appears in more than one count,
or (2) Designate **one sub-report as the single source of truth** for
headcount and reference its value in composite calculations rather than
summing across all sub-reports.

---
---

# QUICK-REFERENCE ANSWER KEY

| Q | Ans | Diff | Q | Ans | Diff | Q | Ans | Diff |
|---|---|---|---|---|---|---|---|---|
| 1 | B | Easy | 21 | C | Med | 41 | A | Med |
| 2 | C | Easy | 22 | C | Med | 42 | B | Med |
| 3 | C | Easy | 23 | B | Med | 43 | B | Hard |
| 4 | C | Easy | 24 | B | Med | 44 | B | Hard |
| 5 | B | Easy | 25 | B | Med | 45 | B | Hard |
| 6 | C | Easy | 26 | B | Med | 46 | B | Hard |
| 7 | B | Easy | 27 | B | Med | 47 | B | Hard |
| 8 | B | Easy | 28 | B | Med | 48 | B | Hard |
| 9 | B | Easy | 29 | B | Med | 49 | B | Hard |
| 10 | B | Easy | 30 | B | Med | 50 | B | Hard |
| 11 | B | Easy | 31 | B | Med | 51 | B | Hard |
| 12 | B | Easy | 32 | B | Med | 52 | B | Hard |
| 13 | C | Easy | 33 | B | Med | 53 | B | Hard |
| 14 | C | Easy | 34 | B | Med | 54 | B | Hard |
| 15 | B | Easy | 35 | B | Med | 55 | B | Hard |
| 16 | B | Easy | 36 | B | Med | 56 | B | Hard |
| 17 | B | Easy | 37 | B | Med | 57 | B | Hard |
| 18 | B | Easy | 38 | B | Med | 58 | B | Hard |
| 19 | B | Easy | 39 | B | Med | 59 | B | Hard |
| 20 | B | Easy | 40 | B | Med | 60 | B | Hard |

---

# COMPOSITE REPORT COMPONENTS CHEAT SHEET

| Component | Purpose |
|---|---|
| **Sub-Report** | Individual report (Advanced/Matrix/Trending) providing data to the composite |
| **Prompt Set** | Common parameters passed to multiple sub-reports; eliminates duplicate prompts |
| **Control Field** | Links composite to sub-reports via a common grouping parameter (usually "Report Type") |
| **Data Column** | Displays raw data from a sub-report field |
| **Calculation Column** | Performs math on other columns (add, subtract, divide, percentage) |
| **Lookup Field Value** | Retrieves additional data via lookup criteria from related objects |
| **Repeating Group** | Creates repeating column patterns for each instance of a group |
| **Empty Column** | Visual spacing and formatting between data columns |
| **Override Conditions** | Conditional display logic (e.g., hide row if value < threshold) |
| **Header / Footer** | Report title, dates, branding at top/bottom of output |

---

# KEY TABS REFERENCE

| Tab | Purpose |
|---|---|
| **General** | Prompt sets, report design, business items |
| **Header/Footer** | Report header and footer content and formatting |
| **Column Headings** | Column header rows, filters, and sorts |
| **Prompts** | Composite-level prompts (distinct from sub-report prompts) |
| **Outcome** | Output delivery method (screen, file, print) |
| **Share** | Security group and user access control |
| **Rows** | Row structure: data rows, calculation rows, section headers |
| **Cells** | Individual cell configuration, formatting, and references |
| **Sub Records** | All linked sub-reports with data sources and filters |
| **Security Domain Name** | Security domain assignment for report access |
| **Override Conditions** | Conditional display rules for dynamic behaviour |

---

*End of Composite Reports Examination -- 60 Questions*
