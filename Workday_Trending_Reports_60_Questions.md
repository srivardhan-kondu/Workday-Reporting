# WORKDAY PRO HCM REPORTING -- TRENDING REPORTS MOCK EXAMINATION

## 60 Exam-Ready Questions

**Exam Code:** Workday-Pro-HCM-Reporting
**Topic Focus:** Trending Reports (~15% of Exam Weightage)
**Print Format:** Black-and-White, A4-Optimised
**Instructions:** Answer all 60 questions. Answer key with explanations is at the END of this document.

---

## SECTION A: TRENDING REPORT FUNDAMENTALS (Q1-Q12)

---

### Question 1

**What is a Trending Report in Workday?**

(A) A report that shows only terminated workers
(B) A report that displays only the most current data at the time of execution
(C) A report limited to financial data
(D) A report specifically designed to track and display changes in worker data over time using periodic snapshots and variance calculations

---

### Question 2

**Which report type is BEST suited for comparing benefit cost by enrolment between the current year and the prior year, with formatted cost and count variance calculations?**

(A) Advanced Report
(B) Matrix Report
(C) Trending Report
(D) Composite Report

---

### Question 3

**Trending Reports in Workday are built on which foundational concept?**

(A) Periodic snapshots of worker data captured and stored at defined intervals
(B) Real-time API calls to external systems
(C) Manual data entry by administrators
(D) Nightly batch imports from a data warehouse

---

### Question 4

**Which of the following metrics is MOST commonly tracked using Trending Reports?**

(A) Individual worker performance scores only
(B) Real-time system uptime
(C) Single-event payroll transaction details
(D) Headcount, turnover, attrition, and workforce composition over time

---

### Question 5

**What distinguishes a Trending Report from an Advanced Report?**

(A) Advanced Reports can track data over time; Trending Reports cannot
(B) Trending Reports are faster to run
(C) There is no meaningful difference
(D) Trending Reports use a time-series data source with periodic snapshots and built-in variance calculations; Advanced Reports use current or effective-dated data

---

### Question 6

**Can a Trending Report display both current data and historical snapshots simultaneously?**

(A) No -- it only shows historical snapshots
(B) Yes -- it can display data across multiple time periods including the most recent snapshot
(C) No -- it only shows the most current data
(D) Yes, but only if a Composite Report wrapper is used

---

### Question 7

**When building a Trending Report, which element is MANDATORY?**

(A) A security policy override
(B) A composite report wrapper
(C) A time period grouping (e.g., year, month) as a row or column parameter
(D) A calculated field

---

### Question 8

**Which grouping options can be applied to columns in a Trending Report?**

(A) Only time periods
(B) Only calculated fields
(C) Worker-related dimensions such as gender, company, cost centre, or supervisory organisation
(D) Only security groups

---

### Question 9

**A "5-Year Headcount Trend" report is an example of which report type?**

(A) Simple Report
(B) Composite Report
(C) Matrix Report (only)
(D) Trending Report

---

### Question 10

**When reporting on headcount within supervisory organisations using trending data, what is CRITICAL to include?**

(A) Only workers hired in the current year
(B) Subordinate organisations to ensure a complete view of headcount
(C) Only the top-level supervisory organisation
(D) Only workers with active status

---

### Question 11

**What is the "Trended Turnover Summary" report used for?**

(A) Managing security group assignments
(B) Configuring business process workflows
(C) Analysing turnover metrics such as Net Gain/Loss, Net Hire Ratio, Voluntary Termination, and Involuntary Termination over specified date ranges
(D) Displaying real-time payroll data

---

### Question 12

**How is the standard attrition rate calculated in Workday Trending Reports?**

(A) Number of terminations over a specified period divided by the average headcount during that period
(B) Total employees divided by total revenue
(C) Number of hires minus number of terminations
(D) Number of open positions divided by total headcount

---

## SECTION B: TRENDED WORKERS DATA SOURCE (Q13-Q22)

---

### Question 13

**What is the "Trended Workers" data source in Workday?**

(A) A data source for integration purposes only
(B) A data source that stores only terminated worker records
(C) A specialised data source that captures periodic snapshots of worker data at defined intervals, enabling time-series reporting
(D) A real-time data source that refreshes every second

---

### Question 14

**Is the Trended Workers data source active by default in a new Workday tenant?**

(A) Yes -- it is active and populated from day one
(B) It depends on the Workday edition
(C) No -- it must be explicitly enabled and populated by running the "Maintain Trended Workers" task
(D) Yes, but only for organisations with more than 500 workers

---

### Question 15

**How often does the Trended Workers data source typically capture snapshots?**

(A) Only when manually triggered
(B) Monthly (end of each month)
(C) Hourly
(D) Annually

---

### Question 16

**What is the maximum default look-back period for trended data in Workday?**

(A) 12 months
(B) 36 months
(C) Unlimited
(D) 72 months (6 years)

---

### Question 17

**What TWO types of records does the Trended Workers data source contain?**

(A) Primary records and secondary records
(B) Parent records and child records
(C) Snapshot records (period-end states) and activity records (events like hires and terminations)
(D) Current records and archived records

---

### Question 18

**Can the Trended Workers data source be used in a non-trending (standard custom) report?**

(A) Yes -- it can be selected as the data source for any custom report
(B) No -- it is exclusively available for trending report types
(C) Yes, but only in composite reports
(D) No -- it can only be used in dashboards

---

### Question 19

**Which field on the Trended Workers data source is used to filter between snapshot records and activity records?**

(A) Worker Status
(B) Organisation Type
(C) Record Type
(D) Report Category

---

### Question 20

**The Trended Workers data source provides an "indexed" structure. What advantage does this provide?**

(A) It allows unlimited data storage
(B) It automatically generates calculated fields
(C) It eliminates the need for security
(D) It provides faster query performance and optimised retrieval compared to non-indexed data sources

---

### Question 21

**A report writer wants to include the worker's compensation rate in a trending report. The compensation field is on the related "Worker" business object, not directly on the Trended Workers data source. What is the recommended approach?**

(A) Create a separate non-trending report for compensation
(B) Add the compensation field directly to the Trended Workers data source to avoid runtime joins
(C) Use a Lookup Related Value calculated field to traverse to the Worker object
(D) Use a Concatenate Text field

---

### Question 22

**What happens if you add a new field to the Trended Workers data source after data has already been collected for prior months?**

(A) All prior snapshots are deleted and must be regenerated
(B) The new field is retroactively populated for all prior snapshots
(C) The new field is available only for future snapshots; prior snapshots will show NULL/blank for that field
(D) The new field is immediately available with current values for all periods

---

## SECTION C: SNAPSHOT VS. ACTIVITY RECORDS (Q23-Q30)

---

### Question 23

**What is a "Snapshot" record in the Trended Workers data source?**

(A) A real-time read of the current database state
(B) A record that exists only in archived backups
(C) A record of a specific event (e.g., a hire or termination)
(D) A point-in-time capture of all workers' data at the end of a defined period (e.g., month-end headcount)

---

### Question 24

**What is an "Activity" record in the Trended Workers data source?**

(A) A record of a specific event that occurred during the period, such as a hire, termination, transfer, or promotion
(B) A period-end summary of all workers
(C) A calculated field result
(D) A security access log entry

---

### Question 25

**You only want to show snapshot data (not activity data) on a custom trending report. What is the MOST efficient approach with minimal performance impact?**

(A) Configure the default value of the Record Type prompt
(B) Run the "Maintain Trended Workers" task and change the default record type
(C) Use the "Trended Workers for Planning" data source filter
(D) Add a report filter using the "Snapshot" field (Record Type = Snapshot)

---

### Question 26

**Why is adding a report-level filter for snapshots preferred over modifying the "Maintain Trended Workers" task?**

(A) Report filters are more secure
(B) Report filters are the only way to filter trending data
(C) There is no preference; both methods are identical
(D) Report filters affect only the individual report, while "Maintain Trended Workers" changes apply system-wide and impact ALL trending reports

---

### Question 27

**An HR analyst wants to see only hire and termination events (not month-end snapshots) in a trending report. How should the report be configured?**

(A) Filter Record Type = Activity, then further filter for Hire and Termination event types
(B) Remove all time-period groupings
(C) Filter Record Type = Snapshot
(D) Use a non-trending data source

---

### Question 28

**In a trending report, snapshot data is useful for which type of analysis?**

(A) Security group membership auditing
(B) Real-time transaction monitoring
(C) Period-end state analysis: "How many workers did we have at the end of each month?"
(D) Individual approval tracking

---

### Question 29

**Activity data in trending reports is useful for which type of analysis?**

(A) Event-based analysis: "How many hires, terminations, or transfers occurred during each period?"
(B) Period-end headcount summaries
(C) Security policy auditing
(D) Report performance monitoring

---

### Question 30

**A trending report displays both snapshot AND activity data. A user notices that headcount numbers appear inflated. What is the MOST LIKELY cause?**

(A) The security policy is incorrect
(B) The trending data is corrupted
(C) Both snapshot records and activity records are being counted together, double-counting workers who both existed at month-end AND had an event during the period
(D) The report has a bug

---

## SECTION D: GROUP BY TIME PERIOD AND VARIANCE (Q31-Q38)

---

### Question 31

**A trending report shows headcount by country trends by quarter. The HR analyst requests monthly granularity instead. What should you change?**

(A) Run the "Maintain Trended Workers" task to change the system-wide trending period
(B) Add a runtime prompt for time period selection
(C) Edit the "Group by Time Period" field in the report definition
(D) Edit the Column Grouping grid in the report definition

---

### Question 32

**What granularity options are available for the "Group by Time Period" setting?**

(A) Only monthly and annually
(B) Monthly, quarterly, and annually
(C) Daily, weekly, monthly, quarterly, and annually
(D) Only quarterly

---

### Question 33

**What is a "variance" in the context of a Trending Report?**

(A) A data entry error
(B) The difference between a report's actual runtime and expected runtime
(C) A security permission difference
(D) The calculated difference between two time periods for a given metric (e.g., headcount in January vs. headcount in February)

---

### Question 34

**A trending report needs to display both the snapshot headcount AND the period-over-period percentage variance. Is this possible in a single report?**

(A) Yes -- trending reports can display metrics alongside calculated variance columns
(B) No -- you need two separate reports
(C) No -- variance can only be displayed in matrix reports
(D) Yes, but only via Prism Analytics

---

### Question 35

**If the "Group by Time Period" is set to "Quarter" and trending data exists for 24 months, how many data points will appear on the report?**

(A) 24 (one per month)
(B) 4 (one per quarter in the most recent year only)
(C) 8 (24 months / 3 months per quarter)
(D) 2 (24 months / 12 months per year)

---

### Question 36

**When trending data is grouped quarterly, which snapshot is used to represent the quarter?**

(A) The first month of the quarter
(B) An average of all three months
(C) The middle month of the quarter
(D) The last month (end) of the quarter

---

### Question 37

**A trending report shows "Net Gain/Loss" as a variance metric. How is this calculated?**

(A) Total compensation minus total benefits cost
(B) Active workers minus inactive workers
(C) Total hires during the period minus total terminations during the period
(D) Current headcount minus budget headcount

---

### Question 38

**What does "Net Hire Ratio" measure in a trending context?**

(A) The ratio of internal promotions to external hires
(B) The ratio of full-time to part-time workers
(C) The ratio of accepted to declined job offers
(D) The ratio of hires to terminations, indicating whether the workforce is growing or shrinking

---

## SECTION E: MAINTAIN TRENDED WORKERS TASK (Q39-Q46)

---

### Question 39

**What is the primary purpose of the "Maintain Trended Workers" task?**

(A) To manage the system-wide trending data collection schedule, organisations included, and configuration parameters
(B) To configure individual trending report definitions
(C) To delete all worker records
(D) To assign security roles to trending report users

---

### Question 40

**When must you run the "Maintain Trended Workers" task? (Select ALL that apply)**

1. When initially enabling trending in the tenant
2. When expanding the look-back period (e.g., from 36 to 72 months)
3. When adding new organisations to the trending data set
4. When changing the trending period from year-month to fiscal schedule

(A) 1 and 2 only
(B) All four (1, 2, 3, and 4)
(C) 1, 2, and 3 only
(D) 1 only

---

### Question 41

**What is the "Number of Periods" field in the "Maintain Trended Workers" task?**

(A) The number of report columns
(B) The number of workers to include
(C) The number of organisations to process
(D) The number of historical monthly snapshots to retain (e.g., 36 means 3 years of monthly data)

---

### Question 42

**You changed the trending period from year-month to fiscal schedule in the "Maintain Trended Workers" task. What happens next?**

(A) All trending reports are automatically deleted
(B) Nothing -- the change takes effect immediately with no data impact
(C) Workday rebuilds the historical trending data based on the new calendar structure; it is recommended to test this in a sandbox first
(D) The change is rejected because trending periods cannot be modified

---

### Question 43

**After running "Maintain Trended Workers," you notice that data is not appearing for the expected periods. What tasks might you need to run?**

(A) "Purge Worker Trending Data" followed by "Create Worker Trending Data" to regenerate the trending dataset
(B) Only re-run "Maintain Trended Workers"
(C) Delete all custom reports and recreate them
(D) Contact Workday to restore from backup

---

### Question 44

**Does the "Maintain Trended Workers" task affect individual report definitions?**

(A) Yes -- it modifies the Group by Time Period setting in all reports
(B) No -- it manages the underlying data infrastructure only; individual report definitions are separate
(C) Yes -- it changes the filters on all existing trending reports
(D) Yes -- it adds new columns to all trending reports

---

### Question 45

**The maximum look-back for Trended Workers was recently expanded. What is the new maximum?**

(A) 24 months (2 years)
(B) 120 months (10 years)
(C) 72 months (6 years)
(D) 36 months (3 years)

---

### Question 46

**Which organisations can be included or excluded from the Trended Workers data set?**

(A) Only supervisory organisations
(B) Only the top-level organisation
(C) Organisations cannot be selectively included or excluded
(D) Any organisations -- the "Maintain Trended Workers" task allows configuration of which organisations are included

---

## SECTION F: PERFORMANCE OPTIMISATION (Q47-Q54)

---

### Question 47

**A trending report using the Trended Workers data source runs slowly because it includes a field from the related "Worker" business object. What is the BEST fix?**

(A) Create a calculated field on the Trended Worker business object
(B) Remove the field and accept the limitation
(C) Run the "Purge Worker Trending Data" task
(D) Add the required field directly to the Trended Workers data source

---

### Question 48

**Which type of filter strategy is recommended for improving trending report performance?**

(A) Apply no filters to see all available data
(B) Use only calculated field-based filters
(C) Use built-in data source prompts instead of report-level filters, as prompts restrict data earlier in processing
(D) Use many "OR" conditions in report-level filters

---

### Question 49

**When optimising a trending report, which filter should be placed FIRST?**

(A) Alphabetically by field name
(B) The least specific filter
(C) The most specific filter that eliminates the largest portion of data
(D) Filter order does not matter

---

### Question 50

**What impact do complex calculated fields have on trending report performance?**

(A) No impact -- calculated fields are pre-computed
(B) Positive impact -- calculated fields always speed up reports
(C) Impact only on non-trending reports
(D) Negative impact -- calculated fields add processing overhead at runtime, increase security checks, and slow report execution

---

### Question 51

**What is the recommended alternative to using many calculated field-based filters in a trending report?**

(A) Remove all filters
(B) Convert to a matrix report
(C) Create an optimised Custom Report Data Source with pre-computed values or use sub-filters and related objects
(D) Add more calculated fields

---

### Question 52

**What is the Workday processing time limit for foreground reports?**

(A) 5 minutes
(B) 30 minutes
(C) 60 minutes
(D) No limit

---

### Question 53

**An administrator wants to schedule a resource-intensive trending report. When should it be scheduled?**

(A) During peak business hours for immediate visibility
(B) At the exact same time as other heavy reports for batch efficiency
(C) Scheduling does not affect performance
(D) During off-peak hours to avoid performance impact on other users

---

### Question 54

**Which Workday tool should you use to diagnose trending report performance issues?**

(A) Business process history
(B) Security audit log
(C) Integration event log
(D) Report Performance Log (showing metrics like Top Level Filter Time, row count, and total runtime)

---

## SECTION G: ADVANCED SCENARIOS AND TROUBLESHOOTING (Q55-Q60)

---

### Question 55

**Scenario: An HR executive complains that a trending headcount report shows different numbers than a standard (non-trending) headcount report run on the same date. What is the MOST LIKELY explanation?**

(A) The trending report uses month-end snapshot data, while the standard report uses real-time current data; if the standard report is run mid-month, the data reflects different points in time
(B) The security policies are different for the two reports
(C) The trending report has a calculation error
(D) One report counts full-time only; the other counts all workers

---

### Question 56

**Scenario: A trending report was working correctly until last week. Now it shows no data for the most recent three months. All prior months display normally. What is the MOST LIKELY cause?**

(A) All workers were terminated
(B) The report was moved to a different security domain
(C) The report definition was changed
(D) The "Maintain Trended Workers" task was modified or failed, stopping the capture of new monthly snapshots

---

### Question 57

**Scenario: An analyst creates a trending report and includes both snapshot AND activity records. The report shows significantly higher headcount than expected. A colleague reviews the report and quickly identifies the issue. What is it?**

(A) The data source is incorrect
(B) The calculated field is wrong
(C) The report is double-counting workers by including them in both snapshot records (period-end state) and activity records (events), inflating the total
(D) The report is missing a filter

---

### Question 58

**Scenario: An administrator added a new field ("Job Family Group") to the Trended Workers data source last month. A report writer builds a trending report using this field for 12-month analysis. The field shows values for the most recent month but is blank for all prior months. Why?**

(A) The field is restricted by security for prior months
(B) The data source does not support this field type
(C) The report has a filter error
(D) The field was added only last month; prior monthly snapshots were captured before the field existed and therefore contain no data for it

---

### Question 59

**Scenario: A trending report is configured with "Group by Time Period = Monthly" and shows 36 data points. The CFO asks to see the same data grouped annually. What changes are needed?**

(A) Create a new report from scratch
(B) Create 3 separate monthly reports (one per year) and sum the results
(C) Change the "Group by Time Period" from "Monthly" to "Annually" in the existing report definition; the 36 monthly data points aggregate into 3 annual data points
(D) Run "Maintain Trended Workers" with an annual schedule

---

### Question 60

**Scenario: The CHRO wants a single dashboard view showing headcount trend (monthly), turnover rate (quarterly), AND detailed hire/termination event data. A single trending report cannot combine all three perspectives. What is the recommended approach?**

(A) Build one very complex trending report with all three perspectives
(B) Use only Workday Prism Analytics
(C) Build three separate reports and print them side by side
(D) Build a Composite Report containing multiple trending sub-reports: one for monthly headcount snapshots, one for quarterly turnover rates, and one for hire/termination activity records

---
---

# ANSWER KEY WITH EXPLANATIONS

---

### Q1 -- Answer: D

A **Trending Report** is specifically designed to track changes in worker data **over time**. It uses periodic snapshots (e.g., month-end captures) and calculates **variances** between periods, enabling HR analysts to identify patterns in headcount, turnover, and compensation changes.

---

### Q2 -- Answer: C

The **Trending Report** is specifically designed for year-over-year or period-over-period comparisons with **built-in variance calculations**. Advanced and Matrix reports provide analytical capabilities but lack built-in time-series snapshot and variance computation.

---

### Q3 -- Answer: A

Trending Reports are built on **periodic snapshots** -- point-in-time captures of worker data stored at defined intervals (typically monthly). These snapshots create a historical record that enables time-series analysis and trend identification.

---

### Q4 -- Answer: D

Trending Reports are most commonly used to track **headcount, turnover, attrition, and workforce composition** over time. These are inherently time-series metrics that require periodic snapshots to measure change.

---

### Q5 -- Answer: D

**Trending Reports** use a specialised **time-series data source** (Trended Workers) that captures periodic snapshots and computes variances between periods. **Advanced Reports** work with current or effective-dated data without built-in snapshot/variance functionality.

---

### Q6 -- Answer: B

Trending Reports display data across **multiple time periods**, including both historical snapshots and the most recent snapshot. This side-by-side comparison is the core value of trending.

---

### Q7 -- Answer: C

A **time period grouping** is mandatory for trending reports. Without a time dimension (e.g., year-month), the report cannot organise data by period and therefore cannot display trends.

---

### Q8 -- Answer: C

While time periods are typically used for row grouping, **columns** can be grouped by worker-related dimensions such as **gender, company, cost centre, supervisory organisation**, or any other relevant attribute.

---

### Q9 -- Answer: D

A "5-Year Headcount Trend" report tracks headcount over 60 monthly snapshots across 5 years. This is a classic **Trending Report** use case leveraging the Trended Workers data source.

---

### Q10 -- Answer: B

When reporting headcount within supervisory organisations, you must include **subordinate organisations** to capture the complete headcount. Excluding subordinates would only show workers directly assigned to the selected org.

---

### Q11 -- Answer: C

The **Trended Turnover Summary** report analyses turnover metrics including **Net Gain/Loss, Net Hire Ratio, Voluntary Termination, and Involuntary Termination** over specified date ranges with organisation and worker type filtering.

---

### Q12 -- Answer: A

The standard attrition calculation is: **Terminations / Average Headcount**. The average headcount is typically the average of the beginning and ending headcount for the period, producing a percentage-based attrition rate.

---

### Q13 -- Answer: C

The **Trended Workers** data source captures **periodic snapshots** of worker data at defined intervals (typically monthly). It stores both snapshot records (period-end states) and activity records (events such as hires and terminations).

---

### Q14 -- Answer: C

The Trended Workers data source is **NOT active by default**. An administrator must explicitly **enable** it and run the **"Maintain Trended Workers"** task to begin capturing snapshots.

---

### Q15 -- Answer: B

The Trended Workers data source typically captures snapshots at the **end of each month**, providing a consistent time-series for headcount tracking and turnover analysis.

---

### Q16 -- Answer: D

Workday has expanded the maximum look-back period for trended data to **72 months (6 years)**. You must update the "Number of Periods" field in the Maintain Trended Workers task.

---

### Q17 -- Answer: C

Two record types: **Snapshot records** (capturing the state of all workers at the end of each period) and **Activity records** (capturing individual events such as hires, terminations, and transfers).

---

### Q18 -- Answer: A

The Trended Workers data source can be selected as the data source for **any custom report**, not just trending reports. However, its full capabilities are best utilised within the trending report framework.

---

### Q19 -- Answer: C

The **"Record Type"** field distinguishes between snapshot records and activity records. Filtering on this field allows you to display only snapshots, only activities, or both.

---

### Q20 -- Answer: D

The indexed structure provides **faster query performance and optimised data retrieval**. Indexed data sources pre-process and organise data for efficient access, critical for trending reports querying large historical datasets.

---

### Q21 -- Answer: B

The recommended approach is to **add required fields directly to the Trended Workers data source**. This avoids runtime joins to related business objects, which significantly degrade trending report performance.

---

### Q22 -- Answer: C

Fields added to the Trended Workers data source are captured in **future snapshots only**. Prior snapshots were taken before the field was added and therefore contain **NULL/blank** values for it.

---

### Q23 -- Answer: D

A **Snapshot record** is a point-in-time capture of every worker's data at the end of a defined period (typically month-end). It represents "how many workers existed and what their attributes were."

---

### Q24 -- Answer: A

An **Activity record** captures a specific **event** that occurred during the period -- a hire, termination, transfer, promotion, or other staffing action.

---

### Q25 -- Answer: D

Adding a **report filter on Record Type = "Snapshot"** is the most efficient approach. It filters already-generated trended data at the report level with **minimal performance impact**.

---

### Q26 -- Answer: D

Report-level filters are scoped to the **individual report**. Modifying the "Maintain Trended Workers" task changes the **system-wide** trending configuration, impacting every trending report in the tenant.

---

### Q27 -- Answer: A

To see only events, filter **Record Type = Activity**. Then add additional filters for specific event types (Hire, Termination) to narrow the results.

---

### Q28 -- Answer: C

Snapshot data is designed for **period-end state analysis**. It answers questions like "How many workers did we have at month-end?" and "How has our workforce composition changed month over month?"

---

### Q29 -- Answer: A

Activity data answers **event-based questions**: "How many new hires occurred in January?", "What was the termination rate by quarter?", "How many transfers happened last fiscal year?"

---

### Q30 -- Answer: C

When both snapshot and activity records are displayed without filtering, workers can appear in **both** record sets -- once as a snapshot and again as an activity event. This **double-counting** inflates headcount.

---

### Q31 -- Answer: C

The **"Group by Time Period"** field in the report definition controls display granularity. Changing it from "Quarter" to "Month" displays monthly data without affecting system-wide configuration.

---

### Q32 -- Answer: B

The "Group by Time Period" setting supports **monthly, quarterly, and annually**. Daily and weekly are not typically available because trending snapshots are captured monthly.

---

### Q33 -- Answer: D

A **variance** is the calculated **difference between two time periods** for a metric. For example, if headcount was 500 in January and 520 in February, the variance is +20.

---

### Q34 -- Answer: A

Trending reports natively support displaying **metrics alongside variance calculations**. You can configure the report to show the snapshot value and the computed variance from the prior period.

---

### Q35 -- Answer: C

With quarterly grouping and 24 months of data, the report aggregates monthly snapshots into **8 quarterly data points** (24 / 3 = 8).

---

### Q36 -- Answer: D

When grouped quarterly, the snapshot from the **last month of the quarter** (March for Q1, June for Q2, September for Q3, December for Q4) is used to represent the quarter-end state.

---

### Q37 -- Answer: C

**Net Gain/Loss** = Hires - Terminations for a given period. A positive value means the organisation gained more workers than it lost.

---

### Q38 -- Answer: D

**Net Hire Ratio** measures the ratio of **hires to terminations**. A ratio greater than 1.0 indicates workforce growth; less than 1.0 indicates contraction.

---

### Q39 -- Answer: A

The **"Maintain Trended Workers"** task manages the **system-wide** trending data infrastructure: which organisations are included, how many periods to retain, and the overall configuration.

---

### Q40 -- Answer: B

**All four** scenarios require running "Maintain Trended Workers": initial enablement, expanding the look-back period, adding organisations, and changing the trending period schedule.

---

### Q41 -- Answer: D

The **"Number of Periods"** field defines how many **historical monthly snapshots** the system retains. Setting it to 36 retains 3 years; 72 retains 6 years (the current maximum).

---

### Q42 -- Answer: C

Changing the trending period schedule causes Workday to **rebuild historical trending data** based on the new calendar structure. Workday strongly recommends **testing in a sandbox** first.

---

### Q43 -- Answer: A

If trending data is not appearing correctly, you may need to **purge** existing data with "Purge Worker Trending Data" and then **regenerate** it with "Create Worker Trending Data."

---

### Q44 -- Answer: B

"Maintain Trended Workers" manages the **underlying data infrastructure** only. It does NOT modify individual report definitions, filters, or display settings.

---

### Q45 -- Answer: C

Workday expanded the maximum look-back period to **72 months (6 years)**. Administrators must update the "Number of Periods" field to utilise the extended history.

---

### Q46 -- Answer: D

The "Maintain Trended Workers" task allows administrators to configure **which organisations are included** in the trending data set, providing control over scope and data volume.

---

### Q47 -- Answer: D

When trending reports pull fields from **related business objects**, Workday performs runtime joins that slow execution. The recommended fix is to **add the field directly to the Trended Workers data source**.

---

### Q48 -- Answer: C

**Built-in data source prompts** restrict data at the **data source level** (earlier in processing), reducing volume before the report engine processes it.

---

### Q49 -- Answer: C

Place the **most selective filter first** -- the one that eliminates the largest portion of data. Subsequent filters then process a smaller dataset.

---

### Q50 -- Answer: D

Complex calculated fields add **runtime processing overhead**. Each calculated field is evaluated at execution time and may trigger additional security checks, multiplied across every snapshot record.

---

### Q51 -- Answer: C

Instead of filtering with calculated fields (which are expensive), create an **optimised Custom Report Data Source** with pre-computed values or use **sub-filters and related objects**.

---

### Q52 -- Answer: B

Workday enforces a **30-minute** limit for foreground reports. Background (scheduled) reports have an extended limit of **6 hours**.

---

### Q53 -- Answer: D

Resource-intensive reports should be scheduled during **off-peak hours** to avoid impacting tenant performance for other users.

---

### Q54 -- Answer: D

The **Report Performance Log** provides detailed execution metrics including **Top Level Filter Time, data source time, total row count, and overall runtime** for diagnosing bottlenecks.

---

### Q55 -- Answer: A

Trending reports use **month-end snapshot data**; standard reports use **real-time current data**. If run mid-month, they reference different points in time, producing different numbers. This is expected behaviour.

---

### Q56 -- Answer: D

If a trending report suddenly stops showing recent data while historical data remains, the most likely cause is that the **"Maintain Trended Workers" task** was modified or **failed to execute** for recent months.

---

### Q57 -- Answer: C

Including both snapshot and activity records without proper filtering causes **double-counting**. The fix is to filter Record Type to show only snapshots (for headcount) or only activities (for events).

---

### Q58 -- Answer: D

Fields added to the Trended Workers data source are captured in **future snapshots only**. Prior snapshots contain no data for the field since it did not exist when they were captured.

---

### Q59 -- Answer: C

Simply change **"Group by Time Period"** from "Monthly" to "Annually." The 36 monthly snapshots aggregate into **3 annual data points**. No new report or system-wide changes required.

---

### Q60 -- Answer: D

A **Composite Report** can combine multiple trending sub-reports: one for monthly headcount snapshots, one for quarterly turnover rates, and one for hire/termination activity records -- all on a single page.

---

# QUICK-REFERENCE ANSWER KEY

| Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | D | 11 | C | 21 | B | 31 | C | 41 | D | 51 | C |
| 2 | C | 12 | A | 22 | C | 32 | B | 42 | C | 52 | B |
| 3 | A | 13 | C | 23 | D | 33 | D | 43 | A | 53 | D |
| 4 | D | 14 | C | 24 | A | 34 | A | 44 | B | 54 | D |
| 5 | D | 15 | B | 25 | D | 35 | C | 45 | C | 55 | A |
| 6 | B | 16 | D | 26 | D | 36 | D | 46 | D | 56 | D |
| 7 | C | 17 | C | 27 | A | 37 | C | 47 | D | 57 | C |
| 8 | C | 18 | A | 28 | C | 38 | D | 48 | C | 58 | D |
| 9 | D | 19 | C | 29 | A | 39 | A | 49 | C | 59 | C |
| 10 | B | 20 | D | 30 | C | 40 | B | 50 | D | 60 | D |

---

*End of Trending Reports Mock Examination -- 60 Questions*
