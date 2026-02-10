# WORKDAY PRO HCM REPORTING -- COMPOSITE REPORTS MOCK EXAMINATION

## 60 Exam-Ready Questions

**Exam Code:** Workday-Pro-HCM-Reporting
**Topic Focus:** Composite Reports (~15% of Exam Weightage)
**Print Format:** Black-and-White, A4-Optimised
**Difficulty:** EASY (Q1-20) | MEDIUM (Q21-42) | HARD (Q43-60)
**Instructions:** Answer all 60 questions. Answer key with explanations is at the END of this document.

---

## SECTION A: EASY -- FUNDAMENTALS (Q1-Q20)

---

### Question 1 [EASY]

**What is a Composite Report in Workday?**

(A) A simple report based on a single data source
(B) A report that can only display matrix data
(C) A report that combines data from multiple sub-reports and data sources into a single consolidated view
(D) A report exclusively used for financial reporting

---

### Question 2 [EASY]

**When creating a new custom report, which report type must you select to build a Composite Report?**

(A) Advanced
(B) Matrix
(C) Simple
(D) Composite

---

### Question 3 [EASY]

**What types of reports can serve as sub-reports within a Composite Report?**

(A) Only Advanced reports
(B) Advanced, Matrix, and Trending reports
(C) Only Matrix reports
(D) Only Simple reports

---

### Question 4 [EASY]

**Which sub-report type is recommended for including dynamic data rows and maintaining sort orders?**

(A) Matrix Report
(B) Trending Report
(C) Simple Report
(D) Advanced Report

---

### Question 5 [EASY]

**Which sub-report type is recommended for summarising data or enabling drill-down capabilities?**

(A) Advanced Report
(B) Trending Report
(C) Matrix Report
(D) Composite Report

---

### Question 6 [EASY]

**Which sub-report type is recommended for analysing data trends over time?**

(A) Advanced Report
(B) Simple Report
(C) Matrix Report
(D) Trending Report

---

### Question 7 [EASY]

**What is a "Prompt Set" in a Composite Report?**

(A) A set of security rules for the report
(B) A list of all available data sources
(C) A common set of selection parameters defined at the composite report level that can be passed to multiple sub-reports
(D) A formatting template for report output

---

### Question 8 [EASY]

**What is the primary purpose of a Prompt Set?**

(A) To improve report security
(B) To add formatting to report output
(C) To restrict which users can run the report
(D) To eliminate duplicate prompts when multiple sub-reports share similar selection parameters

---

### Question 9 [EASY]

**What is a "Control Field" in a Composite Report?**

(A) A field that controls user access
(B) A field that calculates totals
(C) A field that links the composite report to its sub-reports based on a common grouping parameter
(D) A field that formats the report output

---

### Question 10 [EASY]

**The Composite Report designer interface is often compared to which application?**

(A) Microsoft Word
(B) Microsoft Excel / a spreadsheet
(C) Microsoft PowerPoint
(D) Microsoft Access

---

### Question 11 [EASY]

**Can a Composite Report have ZERO sub-reports?**

(A) Yes -- it can display only static text and calculations
(B) Yes -- but only if it uses calculated fields
(C) No -- at least three sub-reports are required
(D) No -- at least one sub-report is required for a functional composite report

---

### Question 12 [EASY]

**Where do you configure the header and footer of a Composite Report?**

(A) In the sub-report definitions
(B) In the security policy
(C) In the Header/Footer tab of the composite report definition
(D) In the data source configuration

---

### Question 13 [EASY]

**How many tabs does a Composite Report definition typically have?**

(A) 3-4 tabs
(B) 5-6 tabs
(C) Only 1 tab
(D) Approximately 15 tabs

---

### Question 14 [EASY]

**Which tab in a Composite Report definition shows all linked sub-reports, their data sources, filters, and primary business items?**

(A) General tab
(B) Sub Records tab
(C) Prompts tab
(D) Outcome tab

---

### Question 15 [EASY]

**What is the "Outcome" tab used for in a Composite Report?**

(A) Defining sub-reports
(B) Setting security permissions
(C) Configuring how the report output is delivered (e.g., screen, file, print)
(D) Adding calculated fields

---

### Question 16 [EASY]

**What is the "Share" tab used for in a Composite Report?**

(A) Defining prompt sets
(B) Configuring data columns
(C) Adding filters
(D) Specifying which security groups or users can access the report

---

### Question 17 [EASY]

**A Composite Report is shared with "HR Business Partners." Can those users automatically see data from all sub-reports?**

(A) Yes -- sharing the composite automatically shares all sub-reports
(B) Yes -- but only if the sub-reports use the same data source
(C) No -- each sub-report must also be shared with the same security groups independently
(D) No -- sub-reports cannot be shared at all

---

### Question 18 [EASY]

**What is a "Data" column type in a Composite Report?**

(A) A column that performs calculations
(B) A column that links to external data sources
(C) A column that displays data pulled directly from a sub-report
(D) A column that shows security information

---

### Question 19 [EASY]

**What is a "Calculation" column type in a Composite Report?**

(A) A column that shows raw data from a sub-report
(B) A column that adds empty space
(C) A column that controls prompt behaviour
(D) A column that performs mathematical operations on other columns (e.g., sum, difference, percentage)

---

### Question 20 [EASY]

**What is an "Empty Column" used for in a Composite Report?**

(A) To display error messages
(B) To store hidden data
(C) For visual formatting and spacing between data columns
(D) To trigger business processes

---

## SECTION B: MEDIUM -- CONFIGURATION AND COMPONENTS (Q21-Q42)

---

### Question 21 [MEDIUM]

**When building a Composite Report, the Control Field is typically set to which business object?**

(A) Worker
(B) Position
(C) Organisation
(D) Report Type

---

### Question 22 [MEDIUM]

**A Composite Report has two sub-reports that both require a "Cost Centre" prompt. Without a Prompt Set, what happens when the user runs the composite report?**

(A) The report fails with an error
(B) The user is prompted TWICE for "Cost Centre" -- once for each sub-report
(C) The system automatically consolidates the prompts
(D) The "Cost Centre" prompt is ignored

---

### Question 23 [MEDIUM]

**When is a Prompt Set explicitly needed (not just automatic consolidation)?**

(A) When sub-reports use the same data source
(B) When the composite report has only one sub-report
(C) When sub-reports use DIFFERENT data sources but share similar selection parameters, or when you need to set default values
(D) When the report has no filters

---

### Question 24 [MEDIUM]

**A sub-report has an "Organisation" prompt left open. What happens in the composite report?**

(A) The prompt is hidden
(B) The sub-report fails
(C) The open prompt automatically appears at the composite report level, allowing the user to select the organisation when running the composite
(D) The prompt defaults to "All Organisations"

---

### Question 25 [MEDIUM]

**What is a "Lookup Field Value" column type used for in a Composite Report?**

(A) Performing arithmetic calculations
(B) Creating empty spacing columns
(C) Defining control fields
(D) Incorporating additional data based on lookup criteria from a related business object

---

### Question 26 [MEDIUM]

**What is a "Repeating Group" column type used for?**

(A) To display static headers
(B) To hide duplicate data
(C) To establish repetition of values across a set of columns, creating a repeating pattern for each instance of a group
(D) To merge cells

---

### Question 27 [MEDIUM]

**Best practice states that each Composite Report should have its own dedicated sub-reports. Why?**

(A) Workday enforces this as a requirement
(B) Sub-reports can only belong to one composite
(C) For security compliance reasons only
(D) Sharing sub-reports across multiple composite reports can lead to performance issues and unintended data changes if the original sub-report is modified

---

### Question 28 [MEDIUM]

**How can you get a comprehensive "one-stop-shop" view of all elements in a Composite Report?**

(A) Export the report to Excel
(B) View the General tab only
(C) Use the "Print" action under Related Actions > Custom Report > Print
(D) Run the report with no prompts

---

### Question 29 [MEDIUM]

**Which tab lists all prompts active on the composite report (distinct from sub-report prompts)?**

(A) General tab
(B) Sub Records tab
(C) Rows tab
(D) Prompts tab

---

### Question 30 [MEDIUM]

**What does the "Rows" tab in a Composite Report configure?**

(A) Report security
(B) Sub-report definitions
(C) The row structure of the report grid, including data rows, calculation rows, section headers, and row-level filters
(D) Prompt sets only

---

### Question 31 [MEDIUM]

**What does the "Cells" tab in a Composite Report configure?**

(A) Only the font colour of cells
(B) Sub-report selections only
(C) Individual cell configurations including data references, calculations, formatting overrides, and conditional formatting
(D) Security domain assignments

---

### Question 32 [MEDIUM]

**A Composite Report needs to display headcount, turnover rate, and open positions. These come from three different data sources. How should you structure the sub-reports?**

(A) Use a single Advanced report with all three data sources
(B) Use only one data source and ignore the other two
(C) Create a single Trending report for all three metrics
(D) Create three separate sub-reports, each using the appropriate data source, and combine them in the composite

---

### Question 33 [MEDIUM]

**A required prompt on a sub-report is not marked with an asterisk in the composite report. What is the MOST LIKELY cause?**

(A) The prompt is optional
(B) The composite report overrides all prompt requirements
(C) For custom prompts, the "Required" checkbox must be explicitly checked on the Prompts tab; Workday only automatically marks Workday-delivered data source requirements
(D) Required prompts do not display asterisks in composite reports

---

### Question 34 [MEDIUM]

**How do you convert a sub-report filter into a composite-level prompt?**

(A) Delete the filter and recreate it as a new prompt
(B) Filters cannot become prompts
(C) On the sub-report filter, select "Prompt the user for the value" instead of providing a default value; the prompt then surfaces at the composite level
(D) Add the filter to the Prompt Set

---

### Question 35 [MEDIUM]

**A Composite Report has an Advanced sub-report and a Matrix sub-report. The Advanced sub-report shows detailed worker records. The Matrix sub-report summarises the same data with drill-down. Is this a valid configuration?**

(A) No -- you cannot mix sub-report types
(B) No -- Matrix reports cannot be sub-reports
(C) Yes, but only if they use the same data source
(D) Yes -- combining Advanced (detail) and Matrix (summary with drill-down) sub-reports is a common and valid composite report pattern

---

### Question 36 [MEDIUM]

**What is the "Override Conditions" tab used for in a Composite Report?**

(A) Overriding security policies
(B) Overriding sub-report filters
(C) Defining conditional logic that alters the report's display behaviour based on runtime conditions (e.g., hiding rows if values are zero)
(D) Overriding prompt default values

---

### Question 37 [MEDIUM]

**A Composite Report is configured with three sub-reports from different data sources. The user runs the report and sees data from only two of the three sub-reports. The third section is blank. What should you check FIRST?**

(A) The composite report's calculated fields
(B) The report's header and footer configuration
(C) The output format setting
(D) Whether the user has security access (domain security) to the third sub-report's data source and fields

---

### Question 38 [MEDIUM]

**Can a Composite Report include drill-to-report links?**

(A) No -- drill-down is not available in composite reports
(B) Only if all sub-reports are Matrix type
(C) Yes -- you can configure drill-to-report links within composite report columns, allowing users to click through to detailed reports
(D) Only through calculated fields

---

### Question 39 [MEDIUM]

**What is the "Column Headings" tab used for?**

(A) Defining calculated fields
(B) Adding sub-reports
(C) Listing column heading rows and their filter/sort options, controlling how column headers are displayed and organised
(D) Configuring security

---

### Question 40 [MEDIUM]

**A Composite Report needs to display data from multiple time periods side by side (e.g., Q1 vs Q2 vs Q3). Which sub-report type is BEST for this?**

(A) Advanced Report with three separate queries
(B) Matrix Report with no groupings
(C) Trending Report configured with quarterly grouping
(D) Simple Report

---

### Question 41 [MEDIUM]

**What is the "Security Domain Name" tab used for in a Composite Report?**

(A) Listing all security groups in the tenant
(B) Assigning the report to a security domain that controls which users can access it
(C) Configuring row-level security
(D) Defining calculated field security

---

### Question 42 [MEDIUM]

**A Composite Report has a Prompt Set with "Organisation" and "Effective Date." Sub-Report A uses both prompts. Sub-Report B only uses "Organisation." What happens to the "Effective Date" prompt for Sub-Report B?**

(A) Sub-Report B fails because it does not use "Effective Date"
(B) The entire composite report fails
(C) Sub-Report B automatically creates a new "Effective Date" filter
(D) The "Effective Date" prompt value is passed to Sub-Report B but ignored because Sub-Report B has no corresponding filter for it

---

## SECTION C: HARD -- ADVANCED SCENARIOS AND TROUBLESHOOTING (Q43-Q60)

---

### Question 43 [HARD]

**Scenario: A report writer builds a Composite Report with Sub-Report A (Advanced) and Sub-Report B (Matrix). Sub-Report A is shared with "HR Partners" and "HR Admins." Sub-Report B is shared with "HR Admins" only. The composite report is shared with "HR Partners." What does an HR Partner user see when they run the composite report?**

(A) They see data from both Sub-Report A and Sub-Report B
(B) The report fails with a security error
(C) They see Sub-Report B only
(D) They see data from Sub-Report A only; Sub-Report B's section is blank because they lack access to it

---

### Question 44 [HARD]

**Scenario: A Composite Report has three sub-reports all using the "Workers for HCM Reporting" data source. The user reports seeing duplicate prompts for "Supervisory Organisation" when running the report. However, Workday should auto-consolidate identical prompts. What is the MOST LIKELY cause?**

(A) Workday has a bug
(B) Duplicate prompts are always expected
(C) The prompts in the different sub-reports are configured with slightly different labels, field references, or filter conditions, preventing Workday from recognising them as identical
(D) The data source does not support prompt consolidation

---

### Question 45 [HARD]

**Scenario: A Composite Report includes a Calculation column that divides "Revenue" (from Sub-Report A) by "Headcount" (from Sub-Report B). For one department, headcount is zero. What happens?**

(A) The report displays zero
(B) The report fails entirely
(C) The value defaults to 1.0
(D) The cell displays an error, NULL, or blank depending on configuration; this is a division-by-zero scenario

---

### Question 46 [HARD]

**Scenario: A Composite Report has a sub-report that is also used as a standalone report by another team. A colleague modifies the standalone sub-report by adding new filters. The Composite Report now shows different data than expected. What happened?**

(A) The composite report's cache is stale
(B) The data source was changed
(C) Because the sub-report is shared between the composite and standalone usage, the filter changes to the standalone sub-report affected the composite report's data as well
(D) A security policy was updated

---

### Question 47 [HARD]

**Scenario: A Composite Report with 5 sub-reports runs very slowly (over 10 minutes). The report performance log shows that Sub-Report 3 takes 8 minutes. What is your recommended troubleshooting approach?**

(A) Delete all sub-reports and rebuild from scratch
(B) Switch Sub-Report 3 from Advanced to Matrix type
(C) Investigate Sub-Report 3 independently: check its data source efficiency, filter configuration, number of fields, calculated field complexity, and whether it includes unnecessary fields not used by the composite
(D) Increase the system timeout limit

---

### Question 48 [HARD]

**Scenario: A Composite Report needs to display employee data alongside their compensation AND benefits information. Compensation uses the "Compensation" data source. Benefits uses the "Benefits" data source. Employee demographics use the "Workers" data source. How should this be structured?**

(A) Create one sub-report with all three data sources
(B) Use only the Workers data source and ignore compensation and benefits
(C) Create a single matrix report
(D) Create three sub-reports (one per data source) and combine them in the composite report, using the worker as the common linking element

---

### Question 49 [HARD]

**Scenario: An analyst configures a Composite Report with a Prompt Set that includes "Organisation" and "Date Range." One sub-report uses a different field path for "Organisation" than the other two sub-reports. The Prompt Set value is not being passed correctly to that sub-report. Why?**

(A) Prompt Sets do not support "Organisation" prompts
(B) Prompt Sets can only pass values to two sub-reports
(C) The sub-report is corrupted
(D) The Prompt Set maps its prompt value to a specific field path; if a sub-report's "Organisation" field uses a different path than the one configured in the Prompt Set, the mapping fails

---

### Question 50 [HARD]

**Scenario: A Composite Report shows "N/A" in several cells where data is expected. The sub-reports run correctly when executed independently. What should you investigate?**

(A) The composite report's formatting settings
(B) The data source indexing
(C) The cell-to-sub-report field mapping in the Cells tab -- incorrect references produce N/A or blank; also verify the Control Field and row-to-sub-report linkage is correct
(D) The Workday tenant configuration

---

### Question 51 [HARD]

**Scenario: A financial controller needs a Composite Report that acts as a Profit & Loss statement. It should show Revenue (from one data source), Cost of Goods Sold (from another), and calculate Gross Profit (Revenue minus COGS). Where is the Gross Profit calculation defined?**

(A) In a sub-report
(B) In a separate calculated field
(C) As a Calculation row/column in the composite report itself, referencing the Revenue and COGS data columns
(D) In the data source

---

### Question 52 [HARD]

**Scenario: A Composite Report has conditional column outlining configured. After adding a new cell with an unexpected conditional value, the column outlining stops working. What should you try?**

(A) Rebuild the entire composite report
(B) Change the report type to Advanced
(C) Delete and recreate the affected repeating column groups or associated rows to reset the conditional behaviour
(D) Remove all sub-reports

---

### Question 53 [HARD]

**Scenario: A Composite Report needs to show year-over-year headcount comparison (Current Year vs. Prior Year) with variance. You have 24 months of trending data. What is the MOST efficient approach?**

(A) Create two separate Advanced sub-reports with manual date filters
(B) Create two composite reports and compare them manually
(C) Create a single Trending sub-report with "Group by Time Period = Annual" and include it in the composite report; the trending report natively handles the year-over-year comparison with built-in variance
(D) Use a calculated field to compute variance in the composite

---

### Question 54 [HARD]

**Scenario: A Composite Report in production has 8 sub-reports and runs in 25 minutes (approaching the 30-minute foreground limit). What are TWO recommended actions?**

(A) Accept the performance and hope it does not degrade further
(B) Delete 4 sub-reports to reduce execution time
(C) Schedule the report as a background process (6-hour limit) AND optimise the slowest sub-reports by reviewing data sources, filters, and calculated field complexity
(D) Convert the composite to a matrix report

---

### Question 55 [HARD]

**Scenario: A Composite Report needs to display a financial summary where some rows should only appear if their value exceeds a threshold (e.g., hide expense lines under $1,000). How is this configured?**

(A) By deleting rows with small values from the sub-report
(B) By adding a filter to the sub-report (which only filters source data, not calculated composite rows)
(C) Using the Override Conditions tab to add a conditional rule that hides rows when the value is below the threshold
(D) This is not possible in Workday

---

### Question 56 [HARD]

**Scenario: A CHRO requests a composite dashboard showing: (1) Headcount trend by month, (2) Turnover rate by quarter, (3) Top 10 open positions, and (4) Employee demographics summary. How should the sub-reports be structured?**

(A) One single sub-report covering everything
(B) Two sub-reports only
(C) Use a worklet instead
(D) Four sub-reports: (1) Trending Report for monthly headcount, (2) Trending Report for quarterly turnover, (3) Advanced Report for open positions with sort/limit, (4) Matrix Report for demographics summary

---

### Question 57 [HARD]

**Scenario: A Composite Report was running correctly. After a Workday update, users report that a previously visible Calculation column now shows blank values. The formula is: "Column A / Column B." Column A and Column B still show correct values. What should you check?**

(A) Whether the Workday update changed the formula syntax
(B) Whether the sub-reports were deleted
(C) Whether the security policy was changed
(D) Whether the cell references in the Calculation column are still valid -- Workday updates can occasionally reset or invalidate cell references in composite calculations; re-verify and reconfigure the cell references

---

### Question 58 [HARD]

**Scenario: You need to add a new sub-report to an existing Composite Report. After adding it, users report that the composite report now takes twice as long to run. The new sub-report runs in under 30 seconds independently. What could cause this?**

(A) The composite report has a hard limit on sub-reports
(B) Adding sub-reports always doubles execution time
(C) The new sub-report may include fields, security checks, or data source joins that interact poorly with the composite's existing configuration; additionally, the sub-report may include many fields not needed by the composite, adding unnecessary processing overhead
(D) The report needs to be deleted and recreated

---

### Question 59 [HARD]

**Scenario: A Composite Report uses Prompt Set A with "Company" and "Date." A new requirement asks for Sub-Report C to be added, which needs a "Location" prompt not relevant to the other sub-reports. How should you configure the prompts?**

(A) Add "Location" to Prompt Set A (forcing all users to select Location even though other sub-reports do not need it)
(B) Create a second composite report for Sub-Report C
(C) Remove the Prompt Set entirely
(D) Leave the "Location" prompt as an open prompt on Sub-Report C; it will automatically surface at the composite level without affecting the other sub-reports or the existing Prompt Set

---

### Question 60 [HARD]

**Scenario: An auditor notices that a Composite Report shows different headcount figures than the HR system's official count. After investigation, you discover the composite uses three sub-reports that each count workers independently. Some workers appear in multiple sub-reports due to overlapping data source criteria. What is the root cause and fix?**

(A) The data is corrupted
(B) The composite calculations are wrong
(C) Security is filtering out some workers
(D) The root cause is overlapping data source criteria across sub-reports, causing the same workers to be counted multiple times. The fix is to ensure each sub-report uses mutually exclusive criteria (non-overlapping filters) or to use a single authoritative sub-report for headcount and reference its values in the composite calculations

---
---

# ANSWER KEY WITH EXPLANATIONS

---

### Q1 -- Answer: C

A **Composite Report** combines data from **multiple sub-reports and data sources** into a single consolidated view. It acts as a container integrating different report types (Advanced, Matrix, Trending).

---

### Q2 -- Answer: D

Select **"Composite"** as the report type during "Create Custom Report." This activates the composite report designer with its unique tabs and configuration options.

---

### Q3 -- Answer: B

Composite Reports can include: **Advanced** (dynamic data rows), **Matrix** (summarised/drill-down data), and **Trending** (time-series analysis) reports.

---

### Q4 -- Answer: D

**Advanced Reports** are recommended for dynamic data rows and maintaining sort orders within a composite report.

---

### Q5 -- Answer: C

**Matrix Reports** are ideal for data summarisation and drill-down, presenting cross-tabulated summaries.

---

### Q6 -- Answer: D

**Trending Reports** are specifically designed for time-series analysis -- tracking data over monthly, quarterly, or annual periods using the Trended Workers data source.

---

### Q7 -- Answer: C

A **Prompt Set** defines common selection parameters at the composite level. It collects values (e.g., organisation, date range) and passes them to relevant sub-reports, eliminating duplicates.

---

### Q8 -- Answer: D

The primary purpose is to **eliminate duplicate prompts**. Without it, users would be prompted separately for each sub-report that shares the same parameter.

---

### Q9 -- Answer: C

A **Control Field** links the composite report to its sub-reports via a common grouping parameter, defining how data is pulled and organised from each sub-report.

---

### Q10 -- Answer: B

The designer is compared to **Microsoft Excel / a spreadsheet** -- a grid-based interface with rows, columns, and cells for data placement.

---

### Q11 -- Answer: D

A composite report requires **at least one sub-report** to function. Without sub-reports, there is no data source.

---

### Q12 -- Answer: C

Configure in the **Header/Footer tab** to add titles, dates, logos, and contextual information at the top and bottom of the report.

---

### Q13 -- Answer: D

A Composite Report has approximately **15 tabs**: General, Header/Footer, Column Headings, Prompts, Outcome, Share, Rows, Cells, Security Domain Name, Sub Records, Override Conditions, and more.

---

### Q14 -- Answer: B

The **Sub Records tab** provides a comprehensive overview of all linked sub-reports, their data sources, filters, and primary business items.

---

### Q15 -- Answer: C

The **Outcome tab** configures output delivery: on-screen viewing, file download (Excel, PDF), or print.

---

### Q16 -- Answer: D

The **Share tab** specifies which **security groups or users** can access the composite report. Both the composite and its sub-reports must be shared.

---

### Q17 -- Answer: C

Sharing the composite does NOT automatically share sub-reports. **Each sub-report must be independently shared**. Users without sub-report access see empty sections.

---

### Q18 -- Answer: C

A **"Data" column** displays data pulled directly from a sub-report, mapping a specific field to a column in the grid.

---

### Q19 -- Answer: D

A **"Calculation" column** performs mathematical operations on data from other columns -- addition, subtraction, multiplication, division, percentages.

---

### Q20 -- Answer: C

**Empty Columns** are used purely for **formatting and visual spacing** to improve readability.

---

### Q21 -- Answer: D

The Control Field is typically set to **"Report Type"**, a standard Workday object that acts as the bridge between the composite and its sub-reports.

---

### Q22 -- Answer: C

Workday **automatically consolidates** duplicate prompts. Identical prompts are presented once, with the value applied to all sub-reports. Prompt Sets provide explicit control for more complex scenarios.

---

### Q23 -- Answer: C

Prompt Sets are needed when sub-reports use **different data sources** but share parameters (auto-consolidation doesn't work across different data sources), or when you need **default values**.

---

### Q24 -- Answer: C

An open (unfilled) sub-report prompt **automatically surfaces** at the composite level, letting the user provide a value at runtime.

---

### Q25 -- Answer: D

A **"Lookup Field Value"** column incorporates additional data from a related business object via lookup criteria, enabling display of data not directly in any sub-report.

---

### Q26 -- Answer: C

**Repeating Groups** create a pattern of columns that repeats for each instance of a grouping element (e.g., per month, per department).

---

### Q27 -- Answer: D

Sharing sub-reports causes two problems: (1) **performance degradation** from unnecessary fields and (2) **unintended changes** when someone modifies a shared sub-report. Dedicated sub-reports provide isolation.

---

### Q28 -- Answer: C

**Related Actions > Custom Report > Print** generates a comprehensive overview of all tabs and configurations -- the "one-stop-shop" view.

---

### Q29 -- Answer: D

The **Prompts tab** lists prompts active at the composite level, distinct from sub-report prompts.

---

### Q30 -- Answer: C

The **Rows tab** configures the complete row structure: data rows, calculation rows, section headers, and row-level filters.

---

### Q31 -- Answer: C

The **Cells tab** provides granular control over individual cells: data references, calculations, formatting overrides, and conditional formatting rules.

---

### Q32 -- Answer: D

Create **three separate sub-reports**, each using its appropriate data source, and combine them in the composite. This is the fundamental purpose of composite reporting.

---

### Q33 -- Answer: C

For **custom prompts**, the "Required" checkbox must be explicitly checked on the Prompts tab. Workday only automatically marks delivered data source requirements.

---

### Q34 -- Answer: C

On the sub-report filter, select **"Prompt the user for the value"** -- this surfaces the filter as a prompt at the composite level.

---

### Q35 -- Answer: D

Combining Advanced (detail) and Matrix (summary with drill-down) sub-reports is a **common and valid pattern** for composite reports.

---

### Q36 -- Answer: C

The **Override Conditions tab** defines conditional display logic: hiding rows if values are zero, changing formatting based on thresholds, or altering cell content based on runtime conditions.

---

### Q37 -- Answer: D

Check **security access** first. If the user lacks access to the third sub-report's **security domain**, that section displays as blank.

---

### Q38 -- Answer: C

Composite reports support **drill-to-report links** configured within column definitions, allowing users to click through to detailed reports.

---

### Q39 -- Answer: C

The **Column Headings tab** configures how column headers are displayed, including heading text, grouping, filter options, and sort behaviour.

---

### Q40 -- Answer: C

A **Trending Report** with quarterly grouping natively organises data by period and displays Q1, Q2, and Q3 side by side.

---

### Q41 -- Answer: B

The **Security Domain Name tab** assigns the report to a security domain. Users must have domain access to run the report.

---

### Q42 -- Answer: D

Workday passes Prompt Set values to all sub-reports. If a sub-report has **no corresponding filter**, it simply **ignores** the value without error.

---

### Q43 -- Answer: D

HR Partner has access to the composite and Sub-Report A, but NOT Sub-Report B. Workday renders A's data and shows **blank** for B's section. Fix: share Sub-Report B with "HR Partners."

---

### Q44 -- Answer: C

Workday auto-consolidates only **identical** prompts (same field reference, label, conditions). **Slightly different configurations** prevent recognition as identical. Fix: standardise or use a Prompt Set.

---

### Q45 -- Answer: D

Division by zero produces **NULL/blank or an error** in the affected cell. The rest of the report renders normally. Add conditional logic to handle zero-headcount scenarios.

---

### Q46 -- Answer: C

This is why **dedicated sub-reports** are recommended. Modifications made for standalone usage affected the composite. Fix: create a dedicated copy for the composite.

---

### Q47 -- Answer: C

Focus on **Sub-Report 3** (the bottleneck). Check: data source efficiency, filter configuration, field count, calculated field complexity, and unnecessary fields.

---

### Q48 -- Answer: D

Create **three dedicated sub-reports** (Workers, Compensation, Benefits) and combine them in the composite, with the worker as the common linking element.

---

### Q49 -- Answer: D

Prompt Sets map to **specific field paths**. If a sub-report uses a different relationship path, the mapping fails. Fix: align field paths or configure separate prompt mappings.

---

### Q50 -- Answer: C

Check the **cell-to-sub-report field mapping** in the Cells tab. Verify the Control Field and row-to-sub-report linkage. Misconfigurations produce N/A even when underlying data exists.

---

### Q51 -- Answer: C

Gross Profit is a **cross-sub-report calculation** defined as a **Calculation row/column** in the composite, referencing Revenue and COGS data columns.

---

### Q52 -- Answer: C

**Delete and recreate** the affected repeating column groups or rows to reset the conditional logic, clearing conflicting configurations.

---

### Q53 -- Answer: C

A **single Trending sub-report** with annual grouping natively displays year-over-year data with built-in variance. Far more efficient than separate reports.

---

### Q54 -- Answer: C

Two actions: (1) **Schedule as background** (6-hour limit) and (2) **optimise slowest sub-reports** by reviewing data sources, filters, and calculated field complexity.

---

### Q55 -- Answer: C

Use the **Override Conditions tab** to add conditional rules: IF value < threshold THEN hide row. This dynamically controls visibility at runtime.

---

### Q56 -- Answer: D

**Four sub-reports**: (1) Trending for monthly headcount, (2) Trending for quarterly turnover, (3) Advanced for open positions, (4) Matrix for demographics summary.

---

### Q57 -- Answer: D

Workday updates can affect **cell references** in composite calculations. **Re-verify and reconfigure** the cell references to ensure they point to correct source cells.

---

### Q58 -- Answer: C

A sub-report may include **many unnecessary fields**, triggering additional security checks and data source joins. Fix: create a **dedicated, lean sub-report** with only needed fields.

---

### Q59 -- Answer: D

Leave "Location" as an **open prompt on Sub-Report C** only. It surfaces at the composite level alongside Prompt Set prompts without affecting other sub-reports.

---

### Q60 -- Answer: D

**Overlapping criteria** cause workers to be counted multiple times. Fix: use **mutually exclusive filters** or designate a **single authoritative sub-report** for headcount.

---

# QUICK-REFERENCE ANSWER KEY

| Q | Ans | Diff | Q | Ans | Diff | Q | Ans | Diff |
|---|---|---|---|---|---|---|---|---|
| 1 | C | Easy | 21 | D | Med | 41 | B | Med |
| 2 | D | Easy | 22 | C | Med | 42 | D | Med |
| 3 | B | Easy | 23 | C | Med | 43 | D | Hard |
| 4 | D | Easy | 24 | C | Med | 44 | C | Hard |
| 5 | C | Easy | 25 | D | Med | 45 | D | Hard |
| 6 | D | Easy | 26 | C | Med | 46 | C | Hard |
| 7 | C | Easy | 27 | D | Med | 47 | C | Hard |
| 8 | D | Easy | 28 | C | Med | 48 | D | Hard |
| 9 | C | Easy | 29 | D | Med | 49 | D | Hard |
| 10 | B | Easy | 30 | C | Med | 50 | C | Hard |
| 11 | D | Easy | 31 | C | Med | 51 | C | Hard |
| 12 | C | Easy | 32 | D | Med | 52 | C | Hard |
| 13 | D | Easy | 33 | C | Med | 53 | C | Hard |
| 14 | B | Easy | 34 | C | Med | 54 | C | Hard |
| 15 | C | Easy | 35 | D | Med | 55 | C | Hard |
| 16 | D | Easy | 36 | C | Med | 56 | D | Hard |
| 17 | C | Easy | 37 | D | Med | 57 | D | Hard |
| 18 | C | Easy | 38 | C | Med | 58 | C | Hard |
| 19 | D | Easy | 39 | C | Med | 59 | D | Hard |
| 20 | C | Easy | 40 | C | Med | 60 | D | Hard |

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

*End of Composite Reports Mock Examination -- 60 Questions*
