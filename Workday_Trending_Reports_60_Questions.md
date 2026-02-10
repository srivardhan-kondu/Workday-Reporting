# WORKDAY PRO HCM REPORTING -- TRENDING REPORTS EXAMINATION

## 60 Exam-Ready Questions with Answers and Explanations

**Exam Code:** Workday-Pro-HCM-Reporting
**Topic Focus:** Trending Reports (~15% of Exam Weightage)
**Print Format:** Black-and-White, A4-Optimised

---

> **Prepared by:** Senior Chief Examiner, Workday Reporting Certification
>
> These 60 questions cover every testable area of Trending Reports: the Trended
> Workers data source, snapshot vs. activity records, Group by Time Period,
> Maintain Trended Workers task, variance calculations, performance optimisation,
> headcount and turnover trending, filtering, prompts, calculated fields in
> trending contexts, and scenario-based troubleshooting.

---

## TABLE OF CONTENTS

- Section A: Trending Report Fundamentals (Q1-Q12)
- Section B: Trended Workers Data Source (Q13-Q22)
- Section C: Snapshot vs. Activity Records (Q23-Q30)
- Section D: Group by Time Period and Variance (Q31-Q38)
- Section E: Maintain Trended Workers Task (Q39-Q46)
- Section F: Performance Optimisation (Q47-Q54)
- Section G: Advanced Scenarios and Troubleshooting (Q55-Q60)

---
---

# SECTION A: TRENDING REPORT FUNDAMENTALS

---

### Question 1

**What is a Trending Report in Workday?**

(A) A report that displays only the most current data at the time of execution
(B) A report specifically designed to track and display changes in worker
data over time using periodic snapshots and variance calculations
(C) A report that shows only terminated workers
(D) A report limited to financial data

**Correct Answer: (B)**

**Explanation:**
A **Trending Report** is specifically designed to track changes in worker data
**over time**. It uses periodic snapshots (e.g., month-end captures) and
calculates **variances** between periods, enabling HR analysts to identify
patterns, trends, and anomalies in workforce data such as headcount, turnover,
and compensation changes.

---

### Question 2

**Which report type is BEST suited for comparing benefit cost by enrolment
between the current year and the prior year, with formatted cost and count
variance calculations?**

(A) Advanced Report
(B) Matrix Report
(C) Composite Report
(D) Trending Report

**Correct Answer: (D)**

**Explanation:**
The **Trending Report** is specifically designed for year-over-year or
period-over-period comparisons with **built-in variance calculations**.
While Advanced and Matrix reports provide analytical capabilities, they
typically use current or effective-dated data rather than time-series
snapshots with automatic variance computation.

---

### Question 3

**Trending Reports in Workday are built on which foundational concept?**

(A) Real-time API calls to external systems
(B) Periodic snapshots of worker data captured and stored at defined
intervals
(C) Manual data entry by administrators
(D) Nightly batch imports from a data warehouse

**Correct Answer: (B)**

**Explanation:**
Trending Reports are built on **periodic snapshots** -- point-in-time captures
of worker data stored at defined intervals (typically monthly). These snapshots
create a historical record that enables time-series analysis, variance
tracking, and trend identification.

---

### Question 4

**Which of the following metrics is MOST commonly tracked using
Trending Reports?**

(A) Individual worker performance scores only
(B) Headcount, turnover, attrition, and workforce composition over time
(C) Real-time system uptime
(D) Single-event payroll transaction details

**Correct Answer: (B)**

**Explanation:**
Trending Reports are most commonly used to track **headcount, turnover,
attrition, and workforce composition** over time. These are inherently
time-series metrics that require periodic snapshots to measure change
and identify patterns.

---

### Question 5

**What distinguishes a Trending Report from an Advanced Report?**

(A) Trending Reports are faster to run
(B) Trending Reports use a time-series data source with periodic snapshots
and built-in variance calculations; Advanced Reports use current or
effective-dated data
(C) Advanced Reports can track data over time; Trending Reports cannot
(D) There is no meaningful difference

**Correct Answer: (B)**

**Explanation:**
**Trending Reports** use a specialised **time-series data source** (Trended
Workers) that captures periodic snapshots and computes variances between
periods. **Advanced Reports** work with current or effective-dated data and
do not have built-in snapshot or variance functionality.

---

### Question 6

**Can a Trending Report display both current data and historical snapshots
simultaneously?**

(A) No -- it only shows historical snapshots
(B) Yes -- it can display data across multiple time periods including
the most recent snapshot
(C) No -- it only shows the most current data
(D) Yes, but only if a Composite Report wrapper is used

**Correct Answer: (B)**

**Explanation:**
Trending Reports display data across **multiple time periods**, including both
historical snapshots and the most recent snapshot. This side-by-side comparison
is the core value of trending: seeing how metrics have changed over time.

---

### Question 7

**When building a Trending Report, which element is MANDATORY?**

(A) A calculated field
(B) A time period grouping (e.g., year, month) as a row or column parameter
(C) A security policy override
(D) A composite report wrapper

**Correct Answer: (B)**

**Explanation:**
A **time period grouping** is mandatory for trending reports. Without a time
dimension (e.g., year-month), the report cannot organise data by period and
therefore cannot display trends. The time period is typically configured as a
row grouping.

---

### Question 8

**Which grouping options can be applied to columns in a Trending Report?**

(A) Only time periods
(B) Worker-related dimensions such as gender, company, cost centre, or
supervisory organisation
(C) Only calculated fields
(D) Only security groups

**Correct Answer: (B)**

**Explanation:**
While time periods are typically used for row grouping, **columns** in a
trending report can be grouped by worker-related dimensions such as **gender,
company, cost centre, supervisory organisation**, or any other relevant
attribute. This creates a cross-tabulated view of trends.

---

### Question 9

**A "5-Year Headcount Trend" report is an example of which report type?**

(A) Simple Report
(B) Trending Report
(C) Composite Report
(D) Matrix Report (only)

**Correct Answer: (B)**

**Explanation:**
A "5-Year Headcount Trend" report tracks headcount over 60 monthly snapshots
across 5 years. This is a classic **Trending Report** use case, leveraging
the Trended Workers data source for time-series headcount analysis.

---

### Question 10

**When reporting on headcount within supervisory organisations using
trending data, what is CRITICAL to include?**

(A) Only the top-level supervisory organisation
(B) Subordinate organisations to ensure a complete view of headcount
(C) Only workers with active status
(D) Only workers hired in the current year

**Correct Answer: (B)**

**Explanation:**
When reporting headcount within supervisory organisations, you must include
**subordinate organisations** to capture the complete headcount. Excluding
subordinates would only show workers directly assigned to the selected org,
missing all workers in child organisations.

---

### Question 11

**What is the "Trended Turnover Summary" report used for?**

(A) Displaying real-time payroll data
(B) Analysing turnover metrics such as Net Gain/Loss, Net Hire Ratio,
Voluntary Termination, and Involuntary Termination over specified date ranges
(C) Managing security group assignments
(D) Configuring business process workflows

**Correct Answer: (B)**

**Explanation:**
The **Trended Turnover Summary** report analyses turnover metrics including
**Net Gain/Loss, Net Hire Ratio, Voluntary Termination, and Involuntary
Termination** over specified date ranges. It supports filtering by supervisory
organisation, worker type, job profile, and management levels.

---

### Question 12

**How is the standard attrition rate calculated in Workday Trending Reports?**

(A) Total employees divided by total revenue
(B) Number of terminations over a specified period divided by the average
headcount during that period
(C) Number of hires minus number of terminations
(D) Number of open positions divided by total headcount

**Correct Answer: (B)**

**Explanation:**
The standard attrition calculation is: **Terminations / Average Headcount**.
The average headcount is typically the average of the beginning and ending
headcount for the period. This produces a percentage-based attrition rate
suitable for trend analysis.

---
---

# SECTION B: TRENDED WORKERS DATA SOURCE

---

### Question 13

**What is the "Trended Workers" data source in Workday?**

(A) A real-time data source that refreshes every second
(B) A specialised data source that captures periodic snapshots of worker
data at defined intervals, enabling time-series reporting
(C) A data source for integration purposes only
(D) A data source that stores only terminated worker records

**Correct Answer: (B)**

**Explanation:**
The **Trended Workers** data source captures **periodic snapshots** of worker
data at defined intervals (typically monthly). It is specifically designed for
trending reports and stores both snapshot records (period-end states) and
activity records (events such as hires and terminations).

---

### Question 14

**Is the Trended Workers data source active by default in a new Workday
tenant?**

(A) Yes -- it is active and populated from day one
(B) No -- it must be explicitly enabled and populated by running the
"Maintain Trended Workers" task
(C) Yes, but only for organisations with more than 500 workers
(D) It depends on the Workday edition

**Correct Answer: (B)**

**Explanation:**
The Trended Workers data source is **NOT active by default**. An administrator
must explicitly **enable** it and run the **"Maintain Trended Workers"** task
to begin capturing snapshots. Without this step, no trending data is available.

---

### Question 15

**How often does the Trended Workers data source typically capture snapshots?**

(A) Hourly
(B) Monthly (end of each month)
(C) Annually
(D) Only when manually triggered

**Correct Answer: (B)**

**Explanation:**
The Trended Workers data source typically captures snapshots at the **end of
each month**. This monthly cadence provides a consistent time-series for
headcount tracking, turnover analysis, and workforce composition trending.

---

### Question 16

**What is the maximum default look-back period for trended data in Workday?**

(A) 12 months
(B) 36 months
(C) 72 months (6 years)
(D) Unlimited

**Correct Answer: (C)**

**Explanation:**
Workday has expanded the maximum look-back period for trended data to **72
months (6 years)**. To access the full 72-month history, you must run the
"Maintain Trended Workers" task and update the "Number of Periods" field.

---

### Question 17

**What TWO types of records does the Trended Workers data source contain?**

(A) Current records and archived records
(B) Snapshot records (period-end states) and activity records (events like
hires and terminations)
(C) Primary records and secondary records
(D) Parent records and child records

**Correct Answer: (B)**

**Explanation:**
The Trended Workers data source contains two record types: **Snapshot records**
(capturing the state of all workers at the end of each period) and **Activity
records** (capturing individual events such as hires, terminations, and
transfers that occurred during each period).

---

### Question 18

**Can the Trended Workers data source be used in a non-trending (standard
custom) report?**

(A) Yes -- it can be selected as the data source for any custom report
(B) No -- it is exclusively available for trending report types
(C) Yes, but only in composite reports
(D) No -- it can only be used in dashboards

**Correct Answer: (A)**

**Explanation:**
The Trended Workers data source can be selected as the data source for
**any custom report**, not just trending reports. However, its full capabilities
(time-period grouping, variance calculations) are best utilised within the
trending report framework.

---

### Question 19

**Which field on the Trended Workers data source is used to filter between
snapshot records and activity records?**

(A) Worker Status
(B) Record Type
(C) Organisation Type
(D) Report Category

**Correct Answer: (B)**

**Explanation:**
The **"Record Type"** field on the Trended Workers data source distinguishes
between snapshot records and activity records. Filtering on this field allows
you to display only snapshots, only activities, or both.

---

### Question 20

**The Trended Workers data source provides an "indexed" structure. What
advantage does this provide?**

(A) It allows unlimited data storage
(B) It provides faster query performance and optimised retrieval compared
to non-indexed data sources
(C) It eliminates the need for security
(D) It automatically generates calculated fields

**Correct Answer: (B)**

**Explanation:**
The indexed structure of the Trended Workers data source provides **faster
query performance and optimised data retrieval**. Indexed data sources
pre-process and organise data for efficient access, which is critical for
trending reports that query large volumes of historical data.

---

### Question 21

**A report writer wants to include the worker's compensation rate in a
trending report. The compensation field is on the related "Worker" business
object, not directly on the Trended Workers data source. What is the
recommended approach?**

(A) Use a Lookup Related Value calculated field to traverse to the Worker object
(B) Add the compensation field directly to the Trended Workers data source
to avoid runtime joins
(C) Create a separate non-trending report for compensation
(D) Use a Concatenate Text field

**Correct Answer: (B)**

**Explanation:**
For trending reports, the recommended approach is to **add required fields
directly to the Trended Workers data source**. This avoids runtime joins to
related business objects, which significantly degrade trending report
performance. The Workday documentation explicitly recommends this approach.

---

### Question 22

**What happens if you add a new field to the Trended Workers data source
after data has already been collected for prior months?**

(A) The new field is retroactively populated for all prior snapshots
(B) The new field is available only for future snapshots; prior snapshots
will show NULL/blank for that field
(C) All prior snapshots are deleted and must be regenerated
(D) The new field is immediately available with current values for all periods

**Correct Answer: (B)**

**Explanation:**
When a new field is added to the Trended Workers data source, it is captured
in **future snapshots only**. Prior snapshots were taken before the field was
added and therefore contain **NULL/blank** values for it. To populate
historical data for the new field, the trending data would need to be
regenerated.

---
---

# SECTION C: SNAPSHOT VS. ACTIVITY RECORDS

---

### Question 23

**What is a "Snapshot" record in the Trended Workers data source?**

(A) A record of a specific event (e.g., a hire or termination)
(B) A point-in-time capture of all workers' data at the end of a defined
period (e.g., month-end headcount)
(C) A real-time read of the current database state
(D) A record that exists only in archived backups

**Correct Answer: (B)**

**Explanation:**
A **Snapshot record** is a point-in-time capture of every worker's data at the
end of a defined period (typically month-end). It represents the "state of the
world" at that moment -- how many workers existed, what their attributes were,
and what organisations they belonged to.

---

### Question 24

**What is an "Activity" record in the Trended Workers data source?**

(A) A period-end summary of all workers
(B) A record of a specific event that occurred during the period, such
as a hire, termination, transfer, or promotion
(C) A calculated field result
(D) A security access log entry

**Correct Answer: (B)**

**Explanation:**
An **Activity record** captures a specific **event** that occurred during the
period -- a hire, termination, transfer, promotion, or other staffing action.
Activity records provide the "what happened" view, while snapshot records
provide the "what it looked like at period end" view.

---

### Question 25

**You only want to show snapshot data (not activity data) on a custom trending
report. What is the MOST efficient approach with minimal performance impact?**

(A) Configure the default value of the Record Type prompt
(B) Use the "Trended Workers for Planning" data source filter
(C) Add a report filter using the "Snapshot" field (Record Type = Snapshot)
(D) Run the "Maintain Trended Workers" task and change the default record type

**Correct Answer: (C)**

**Explanation:**
Adding a **report filter on the Record Type = "Snapshot"** is the most efficient
approach. It filters already-generated trended data at the report level with
**minimal performance impact**. Setting default prompt values (A) may still
retrieve non-snapshot data before filtering. Running "Maintain Trended Workers"
(D) changes system-wide configuration and affects all trending reports.

---

### Question 26

**Why is adding a report-level filter for snapshots preferred over modifying
the "Maintain Trended Workers" task?**

(A) Report filters are more secure
(B) Report filters affect only the individual report, while "Maintain Trended
Workers" changes apply system-wide and impact ALL trending reports
(C) Report filters are the only way to filter trending data
(D) There is no preference; both methods are identical

**Correct Answer: (B)**

**Explanation:**
Report-level filters are scoped to the **individual report**. Modifying the
"Maintain Trended Workers" task changes the **system-wide** trending
configuration, which impacts every trending report in the tenant. For a
single report's requirement, a report-level filter is appropriate and less
disruptive.

---

### Question 27

**An HR analyst wants to see only hire and termination events (not month-end
snapshots) in a trending report. How should the report be configured?**

(A) Filter Record Type = Snapshot
(B) Filter Record Type = Activity, then further filter for Hire and
Termination event types
(C) Remove all time-period groupings
(D) Use a non-trending data source

**Correct Answer: (B)**

**Explanation:**
To see only events, filter **Record Type = Activity**. Then add additional
filters for specific event types (Hire, Termination) to narrow the results.
This shows the individual staffing events rather than period-end snapshots.

---

### Question 28

**In a trending report, snapshot data is useful for which type of analysis?**

(A) Real-time transaction monitoring
(B) Period-end state analysis: "How many workers did we have at the end of
each month?"
(C) Individual approval tracking
(D) Security group membership auditing

**Correct Answer: (B)**

**Explanation:**
Snapshot data is designed for **period-end state analysis**. It answers
questions like "How many workers did we have at month-end?", "What was the
headcount by department at the end of Q3?", and "How has our workforce
composition changed month over month?"

---

### Question 29

**Activity data in trending reports is useful for which type of analysis?**

(A) Period-end headcount summaries
(B) Event-based analysis: "How many hires, terminations, or transfers
occurred during each period?"
(C) Security policy auditing
(D) Report performance monitoring

**Correct Answer: (B)**

**Explanation:**
Activity data answers **event-based questions**: "How many new hires occurred
in January?", "What was the termination rate by quarter?", "How many
transfers happened last fiscal year?" Activity records track the events that
cause changes between snapshots.

---

### Question 30

**A trending report displays both snapshot AND activity data. A user
notices that headcount numbers appear inflated. What is the MOST LIKELY
cause?**

(A) The security policy is incorrect
(B) Both snapshot records and activity records are being counted together,
double-counting workers who both existed at month-end AND had an event
during the period
(C) The trending data is corrupted
(D) The report has a bug

**Correct Answer: (B)**

**Explanation:**
When both snapshot and activity records are displayed without filtering,
workers can appear in **both** record sets -- once as a month-end snapshot and
again as an activity event (e.g., a hire event). This double-counting inflates
headcount. The solution is to filter to **either** snapshots OR activities,
depending on the analysis goal.

---
---

# SECTION D: GROUP BY TIME PERIOD AND VARIANCE

---

### Question 31

**A trending report shows headcount by country trends by quarter. The HR
analyst requests monthly granularity instead. What should you change?**

(A) Edit the Column Grouping grid in the report definition
(B) Edit the "Group by Time Period" field in the report definition
(C) Add a runtime prompt for time period selection
(D) Run the "Maintain Trended Workers" task to change the system-wide
trending period

**Correct Answer: (B)**

**Explanation:**
The **"Group by Time Period"** field in the report definition controls the
granularity of trending data display. Changing it from "Quarter" to "Month"
displays monthly data. This is a report-level change that does not affect
system-wide configuration or other reports.

---

### Question 32

**What granularity options are available for the "Group by Time Period"
setting?**

(A) Only monthly and annually
(B) Monthly, quarterly, and annually
(C) Daily, weekly, monthly, quarterly, and annually
(D) Only quarterly

**Correct Answer: (B)**

**Explanation:**
The "Group by Time Period" setting supports **monthly, quarterly, and annually**
as the primary granularity options. Daily and weekly are not typically available
because trending snapshots are captured monthly.

---

### Question 33

**What is a "variance" in the context of a Trending Report?**

(A) A security permission difference
(B) The calculated difference between two time periods for a given metric
(e.g., headcount in January vs. headcount in February)
(C) A data entry error
(D) The difference between a report's actual runtime and expected runtime

**Correct Answer: (B)**

**Explanation:**
A **variance** in trending reports is the calculated **difference between two
time periods** for a metric. For example, if headcount was 500 in January and
520 in February, the variance is +20. Variances can be expressed as absolute
numbers or percentages.

---

### Question 34

**A trending report needs to display both the snapshot headcount AND the
period-over-period percentage variance. Is this possible in a single report?**

(A) No -- you need two separate reports
(B) Yes -- trending reports can display metrics alongside calculated
variance columns
(C) No -- variance can only be displayed in matrix reports
(D) Yes, but only via Prism Analytics

**Correct Answer: (B)**

**Explanation:**
Trending reports natively support displaying **metrics alongside variance
calculations**. You can configure the report to show the snapshot value (e.g.,
headcount) and the computed variance (absolute or percentage change) from the
prior period in the same output.

---

### Question 35

**If the "Group by Time Period" is set to "Quarter" and trending data exists
for 24 months, how many data points will appear on the report?**

(A) 24 (one per month)
(B) 8 (24 months / 3 months per quarter)
(C) 2 (24 months / 12 months per year)
(D) 4 (one per quarter in the most recent year only)

**Correct Answer: (B)**

**Explanation:**
With quarterly grouping and 24 months of data, the report aggregates monthly
snapshots into **8 quarterly data points** (24 / 3 = 8). Each quarter
consolidates three months of snapshot data.

---

### Question 36

**When trending data is grouped quarterly, which snapshot is used to
represent the quarter?**

(A) The first month of the quarter
(B) The middle month of the quarter
(C) The last month (end) of the quarter
(D) An average of all three months

**Correct Answer: (C)**

**Explanation:**
When grouped quarterly, the snapshot from the **last month of the quarter**
(i.e., March for Q1, June for Q2, September for Q3, December for Q4) is
typically used to represent the quarter-end state. This follows the standard
period-end convention.

---

### Question 37

**A trending report shows "Net Gain/Loss" as a variance metric. How is this
calculated?**

(A) Total compensation minus total benefits cost
(B) Total hires during the period minus total terminations during the period
(C) Current headcount minus budget headcount
(D) Active workers minus inactive workers

**Correct Answer: (B)**

**Explanation:**
**Net Gain/Loss** = Hires - Terminations for a given period. A positive value
means the organisation gained more workers than it lost. A negative value
indicates more departures than arrivals. This metric uses activity-type data.

---

### Question 38

**What does "Net Hire Ratio" measure in a trending context?**

(A) The ratio of internal promotions to external hires
(B) The ratio of hires to terminations, indicating whether the workforce
is growing or shrinking
(C) The ratio of full-time to part-time workers
(D) The ratio of accepted to declined job offers

**Correct Answer: (B)**

**Explanation:**
**Net Hire Ratio** measures the ratio of **hires to terminations**. A ratio
greater than 1.0 indicates workforce growth (more hires than terminations).
A ratio less than 1.0 indicates workforce contraction. This is a key
trend metric for workforce planning.

---
---

# SECTION E: MAINTAIN TRENDED WORKERS TASK

---

### Question 39

**What is the primary purpose of the "Maintain Trended Workers" task?**

(A) To configure individual trending report definitions
(B) To manage the system-wide trending data collection schedule,
organisations included, and configuration parameters
(C) To delete all worker records
(D) To assign security roles to trending report users

**Correct Answer: (B)**

**Explanation:**
The **"Maintain Trended Workers"** task manages the **system-wide** trending
data infrastructure: which organisations are included, how many periods of
data to retain, and the overall trending configuration. It does NOT configure
individual report definitions.

---

### Question 40

**When must you run the "Maintain Trended Workers" task? (Select ALL
that apply)**

1. When initially enabling trending in the tenant
2. When expanding the look-back period (e.g., from 36 to 72 months)
3. When adding new organisations to the trending data set
4. When changing the trending period from year-month to fiscal schedule

**Correct Answer: All four (1, 2, 3, and 4)**

**Explanation:**
All four scenarios require running "Maintain Trended Workers": **initial
enablement**, **expanding the look-back period** (updating the "Number of
Periods" field), **adding organisations**, and **changing the trending period
schedule**. Each of these is a system-wide configuration change.

---

### Question 41

**What is the "Number of Periods" field in the "Maintain Trended Workers"
task?**

(A) The number of report columns
(B) The number of historical monthly snapshots to retain (e.g., 36
means 3 years of monthly data)
(C) The number of workers to include
(D) The number of organisations to process

**Correct Answer: (B)**

**Explanation:**
The **"Number of Periods"** field defines how many **historical monthly
snapshots** the system retains. Setting it to 36 retains 3 years; setting it
to 72 retains 6 years (the current maximum). Increasing this value triggers
the generation of additional historical data.

---

### Question 42

**You changed the trending period from year-month to fiscal schedule in the
"Maintain Trended Workers" task. What happens next?**

(A) Nothing -- the change takes effect immediately with no data impact
(B) Workday rebuilds the historical trending data based on the new calendar
structure; it is recommended to test this in a sandbox first
(C) All trending reports are automatically deleted
(D) The change is rejected because trending periods cannot be modified

**Correct Answer: (B)**

**Explanation:**
Changing the trending period schedule causes Workday to **rebuild historical
trending data** based on the new calendar structure. This is a significant
operation that can impact data integrity and report output. Workday strongly
recommends **testing in a sandbox environment** before applying to production.

---

### Question 43

**After running "Maintain Trended Workers," you notice that data is not
appearing for the expected periods. What tasks might you need to run?**

(A) Only re-run "Maintain Trended Workers"
(B) "Purge Worker Trending Data" followed by "Create Worker Trending Data"
to regenerate the trending dataset
(C) Delete all custom reports and recreate them
(D) Contact Workday to restore from backup

**Correct Answer: (B)**

**Explanation:**
If trending data is not appearing correctly after configuration changes, you
may need to **purge** the existing data with "Purge Worker Trending Data" and
then **regenerate** it with "Create Worker Trending Data." This clears the old
data and rebuilds it based on the updated configuration.

---

### Question 44

**Does the "Maintain Trended Workers" task affect individual report
definitions?**

(A) Yes -- it modifies the Group by Time Period setting in all reports
(B) No -- it manages the underlying data infrastructure only; individual
report definitions are separate
(C) Yes -- it changes the filters on all existing trending reports
(D) Yes -- it adds new columns to all trending reports

**Correct Answer: (B)**

**Explanation:**
"Maintain Trended Workers" manages the **underlying trending data
infrastructure** (data source enablement, period count, org scope). It does
NOT modify individual report definitions, filters, or display settings. Those
are configured separately within each report.

---

### Question 45

**The maximum look-back for Trended Workers was recently expanded. What is
the new maximum?**

(A) 24 months (2 years)
(B) 36 months (3 years)
(C) 72 months (6 years)
(D) 120 months (10 years)

**Correct Answer: (C)**

**Explanation:**
Workday expanded the maximum look-back period to **72 months (6 years)**. To
utilise this extended history, administrators must update the "Number of
Periods" field in the "Maintain Trended Workers" task and allow the system
to generate the additional historical data.

---

### Question 46

**Which organisations can be included or excluded from the Trended Workers
data set?**

(A) Only supervisory organisations
(B) Any organisations -- the "Maintain Trended Workers" task allows
configuration of which organisations are included
(C) Only the top-level organisation
(D) Organisations cannot be selectively included or excluded

**Correct Answer: (B)**

**Explanation:**
The "Maintain Trended Workers" task allows administrators to configure **which
organisations are included** in the trending data set. This provides control
over the scope of trending data collection, allowing organisations to focus
on relevant populations and manage data volume.

---
---

# SECTION F: PERFORMANCE OPTIMISATION

---

### Question 47

**A trending report using the Trended Workers data source runs slowly because
it includes a field from the related "Worker" business object. What is the
BEST fix?**

(A) Create a calculated field on the Trended Worker business object
(B) Run the "Purge Worker Trending Data" task
(C) Add the required field directly to the Trended Workers data source
(D) Remove the field and accept the limitation

**Correct Answer: (C)**

**Explanation:**
When trending reports pull fields from **related business objects**, Workday
must perform runtime joins that slow execution significantly. The recommended
fix is to **add the field directly to the Trended Workers data source** so the
data is pre-joined and indexed. This is explicitly documented as a Workday
best practice.

---

### Question 48

**Which type of filter strategy is recommended for improving trending
report performance?**

(A) Use many "OR" conditions in report-level filters
(B) Use built-in data source prompts instead of report-level filters, as
prompts restrict data earlier in processing
(C) Apply no filters to see all available data
(D) Use only calculated field-based filters

**Correct Answer: (B)**

**Explanation:**
**Built-in data source prompts** restrict data at the **data source level**
(earlier in processing), reducing the volume of data the report engine must
handle. Report-level filters are applied later and process more data before
filtering. Minimising "OR" conditions and calculated field-based filters
further improves performance.

---

### Question 49

**When optimising a trending report, which filter should be placed FIRST?**

(A) The most specific filter that eliminates the largest portion of data
(B) The least specific filter
(C) Alphabetically by field name
(D) Filter order does not matter

**Correct Answer: (A)**

**Explanation:**
Filter order matters for performance. Place the **most selective filter first**
-- the one that eliminates the largest portion of data. This ensures
subsequent filters process a smaller dataset, reducing overall processing time.

---

### Question 50

**What impact do complex calculated fields have on trending report
performance?**

(A) No impact -- calculated fields are pre-computed
(B) Negative impact -- calculated fields add processing overhead at
runtime, increase security checks, and slow report execution
(C) Positive impact -- calculated fields always speed up reports
(D) Impact only on non-trending reports

**Correct Answer: (B)**

**Explanation:**
Complex calculated fields add **runtime processing overhead**. Each calculated
field is evaluated at execution time and may trigger additional security
checks. For trending reports processing large historical datasets, this
overhead is multiplied across every snapshot record. Minimise calculated
fields or use pre-computed values in the data source.

---

### Question 51

**What is the recommended alternative to using many calculated field-based
filters in a trending report?**

(A) Remove all filters
(B) Create an optimised Custom Report Data Source with pre-computed values
or use sub-filters and related objects
(C) Convert to a matrix report
(D) Add more calculated fields

**Correct Answer: (B)**

**Explanation:**
Instead of filtering with calculated fields (which are expensive), create an
**optimised Custom Report Data Source** with pre-computed values or use
**sub-filters and related objects**. This moves the computation from runtime
to the data source level, where it is indexed and cached.

---

### Question 52

**What is the Workday processing time limit for foreground reports?**

(A) 5 minutes
(B) 30 minutes
(C) 60 minutes
(D) No limit

**Correct Answer: (B)**

**Explanation:**
Workday enforces a **30-minute processing limit** for foreground (user-initiated
interactive) reports. Reports exceeding this limit time out. Background
(scheduled) reports have an extended limit of **6 hours**. Trending reports
with large datasets should be scheduled as background processes.

---

### Question 53

**An administrator wants to schedule a resource-intensive trending report.
When should it be scheduled?**

(A) During peak business hours for immediate visibility
(B) During off-peak hours to avoid performance impact on other users
(C) At the exact same time as other heavy reports for batch efficiency
(D) Scheduling does not affect performance

**Correct Answer: (B)**

**Explanation:**
Resource-intensive reports should be scheduled during **off-peak hours** to
avoid impacting tenant performance for other users. Running heavy reports
during peak hours can slow down the entire tenant's responsiveness.

---

### Question 54

**Which Workday tool should you use to diagnose trending report
performance issues?**

(A) Security audit log
(B) Report Performance Log (showing metrics like Top Level Filter Time,
row count, and total runtime)
(C) Integration event log
(D) Business process history

**Correct Answer: (B)**

**Explanation:**
The **Report Performance Log** provides detailed execution metrics including
**Top Level Filter Time, data source time, total row count, and overall
runtime**. It is the primary diagnostic tool for identifying performance
bottlenecks in trending reports.

---
---

# SECTION G: ADVANCED SCENARIOS AND TROUBLESHOOTING

---

### Question 55

**Scenario: An HR executive complains that a trending headcount report shows
different numbers than a standard (non-trending) headcount report run on the
same date. What is the MOST LIKELY explanation?**

(A) The trending report has a calculation error
(B) The trending report uses month-end snapshot data, while the standard
report uses real-time current data; if the standard report is run mid-month,
the data reflects different points in time
(C) The security policies are different for the two reports
(D) One report counts full-time only; the other counts all workers

**Correct Answer: (B)**

**Explanation:**
Trending reports use **month-end snapshot data** (the state at period close).
Standard reports use **real-time current data**. If the standard report is run
on the 15th, it reflects mid-month headcount (including hires and terminations
that occurred since month-end). The two reports reference different points in
time, producing different numbers. This is expected behaviour, not an error.

---

### Question 56

**Scenario: A trending report was working correctly until last week. Now it
shows no data for the most recent three months. All prior months display
normally. What is the MOST LIKELY cause?**

(A) The report definition was changed
(B) The "Maintain Trended Workers" task was modified or failed, stopping
the capture of new monthly snapshots
(C) All workers were terminated
(D) The report was moved to a different security domain

**Correct Answer: (B)**

**Explanation:**
If a trending report suddenly stops showing recent data while historical data
remains intact, the most likely cause is that the **"Maintain Trended Workers"
task** was modified (e.g., organisations removed, the task was disabled) or
**failed to execute** for the recent months. Without the task running, new
monthly snapshots are not captured.

---

### Question 57

**Scenario: An analyst creates a trending report and includes both snapshot
AND activity records. The report shows significantly higher headcount than
expected. A colleague reviews the report and quickly identifies the issue.
What is it?**

(A) The report is missing a filter
(B) The report is double-counting workers by including them in both snapshot
records (period-end state) and activity records (events), inflating the total
(C) The data source is incorrect
(D) The calculated field is wrong

**Correct Answer: (B)**

**Explanation:**
Including both snapshot and activity records without proper filtering causes
**double-counting**. A worker who existed at month-end (snapshot) AND had an
event during the month (activity) appears in both record sets. The fix is to
filter Record Type to show only snapshots (for headcount analysis) or only
activities (for event analysis), not both simultaneously.

---

### Question 58

**Scenario: An administrator added a new field ("Job Family Group") to the
Trended Workers data source last month. A report writer builds a trending
report using this field for 12-month analysis. The field shows values for
the most recent month but is blank for all prior months. Why?**

(A) The report has a filter error
(B) The field was added only last month; prior monthly snapshots were captured
before the field existed and therefore contain no data for it
(C) The field is restricted by security for prior months
(D) The data source does not support this field type

**Correct Answer: (B)**

**Explanation:**
Fields added to the Trended Workers data source are captured in **future
snapshots only**. Prior snapshots were taken before the field was added and
do not contain data for it. To populate historical data, the trending data
would need to be **purged and regenerated** (which may or may not retroactively
populate historical values depending on whether the historical data still
exists in the transactional system).

---

### Question 59

**Scenario: A trending report is configured with "Group by Time Period =
Monthly" and shows 36 data points. The CFO asks to see the same data
grouped annually. What changes are needed?**

(A) Create a new report from scratch
(B) Change the "Group by Time Period" from "Monthly" to "Annually" in the
existing report definition; the 36 monthly data points aggregate into
3 annual data points
(C) Run "Maintain Trended Workers" with an annual schedule
(D) Create 3 separate monthly reports (one per year) and sum the results

**Correct Answer: (B)**

**Explanation:**
Simply change the **"Group by Time Period"** from "Monthly" to "Annually" in
the report definition. The 36 monthly snapshots aggregate into **3 annual
data points**. No new report, system-wide changes, or manual calculations
are required.

---

### Question 60

**Scenario: The CHRO wants a single dashboard view showing headcount trend
(monthly), turnover rate (quarterly), AND detailed hire/termination event
data. A single trending report cannot combine all three perspectives.
What is the recommended approach?**

(A) Build one very complex trending report with all three perspectives
(B) Build a Composite Report containing multiple trending sub-reports:
one for monthly headcount snapshots, one for quarterly turnover rates,
and one for hire/termination activity records
(C) Build three separate reports and print them side by side
(D) Use only Workday Prism Analytics

**Correct Answer: (B)**

**Explanation:**
A **Composite Report** can combine multiple trending sub-reports into a single
unified view. Each sub-report is configured independently: one uses snapshot
records grouped monthly for headcount, another uses snapshot records grouped
quarterly with turnover variance calculations, and a third uses activity
records filtered for hires and terminations. The composite report presents
all three perspectives on a single page, meeting the CHRO's requirement.

---
---

# QUICK-REFERENCE ANSWER KEY

| Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | B | 11 | B | 21 | B | 31 | B | 41 | B | 51 | B |
| 2 | D | 12 | B | 22 | B | 32 | B | 42 | B | 52 | B |
| 3 | B | 13 | B | 23 | B | 33 | B | 43 | B | 53 | B |
| 4 | B | 14 | B | 24 | B | 34 | B | 44 | B | 54 | B |
| 5 | B | 15 | B | 25 | C | 35 | B | 45 | C | 55 | B |
| 6 | B | 16 | C | 26 | B | 36 | C | 46 | B | 56 | B |
| 7 | B | 17 | B | 27 | B | 37 | B | 47 | C | 57 | B |
| 8 | B | 18 | A | 28 | B | 38 | B | 48 | B | 58 | B |
| 9 | B | 19 | B | 29 | B | 39 | B | 49 | A | 59 | B |
| 10 | B | 20 | B | 30 | B | 40 | All | 50 | B | 60 | B |

---

# KEY CONCEPTS CHEAT SHEET

| Concept | Definition |
|---|---|
| **Trended Workers** | Specialised data source capturing periodic worker snapshots and activity events |
| **Snapshot Record** | Point-in-time capture of all workers at period end (e.g., month-end headcount) |
| **Activity Record** | Individual event record (hire, termination, transfer) during a period |
| **Record Type** | Field on Trended Workers data source to filter between snapshots and activities |
| **Group by Time Period** | Report-level setting controlling display granularity (monthly/quarterly/annually) |
| **Variance** | Calculated difference between two consecutive time periods for a metric |
| **Maintain Trended Workers** | System-wide task controlling trending enablement, period count, and org scope |
| **Number of Periods** | Configuration field defining how many months of historical snapshots to retain (max 72) |
| **Net Gain/Loss** | Hires minus Terminations for a period |
| **Net Hire Ratio** | Ratio of Hires to Terminations (>1.0 = growth, <1.0 = contraction) |
| **Attrition Rate** | Terminations / Average Headcount for a period |
| **Purge Worker Trending Data** | Task to clear existing trending data before regeneration |
| **Create Worker Trending Data** | Task to regenerate trending data after purging |
| **Report Performance Log** | Diagnostic tool showing filter time, data source time, row count, and runtime |

---

*End of Trending Reports Examination -- 60 Questions*
