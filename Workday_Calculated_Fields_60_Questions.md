# WORKDAY PRO HCM REPORTING -- CALCULATED FIELDS MOCK EXAMINATION

## 60 Exam-Ready Questions

**Exam Code:** Workday-Pro-HCM-Reporting
**Topic Focus:** Calculated Fields (~25% of Exam Weightage)
**Print Format:** Black-and-White, A4-Optimised
**Instructions:** Answer all 60 questions. Answer key with explanations is at the END of this document.

---

## SECTION A: FUNDAMENTALS AND CONCEPTS (Q1-Q10)

---

### Question 1

**What is a Calculated Field in Workday?**

(A) A field stored permanently in the Workday database
(B) A field that can only be used in integrations
(C) A custom field that derives or transforms data at runtime using existing fields and functions
(D) A system field that cannot be modified

---

### Question 2

**Calculated Fields in Workday are always associated with which of the following?**

(A) A security group
(B) A supervisory organisation
(C) A report only
(D) A business object

---

### Question 3

**Where can Calculated Fields be used in Workday? (Select the BEST answer)**

(A) Only in custom reports
(B) In reports, integrations, business processes, and other configurable areas
(C) Only in integrations
(D) Only in business processes

---

### Question 4

**What is the difference between a system-wide (tenant-level) Calculated Field and a report-specific Calculated Field?**

(A) There is no difference
(B) A report-specific Calculated Field is more performant
(C) A system-wide Calculated Field can only be used in integrations
(D) A system-wide Calculated Field is created via "Create Calculated Field" and can be reused across any report or process on the same business object; a report-specific one is created within a report and is only available in that report

---

### Question 5

**When is a Calculated Field evaluated?**

(A) When the tenant is loaded
(B) Once per day during a batch job
(C) At runtime, each time it is referenced (e.g., when a report is run)
(D) Only during integration executions

---

### Question 6

**Which Workday task is used to create a system-wide Calculated Field?**

(A) Create Custom Report
(B) Maintain Calculated Fields
(C) Create Calculated Field
(D) Build Custom Data Source

---

### Question 7

**A Calculated Field created on the "Worker" business object can access fields from which of the following?**

(A) Only fields directly on the Worker object
(B) Fields on any business object in the tenant
(C) Only fields on the Worker object's parent object
(D) Fields on the Worker object and fields on its related business objects

---

### Question 8

**You have created a system-wide Calculated Field on the "Worker" business object. A colleague wants to use it in a report based on the "Position" business object. Is this possible?**

(A) Yes, directly
(B) Yes, but only if the report is a composite report
(C) No -- the Calculated Field must be on the same business object as the report's primary data source, or accessible via a related object relationship
(D) No -- Calculated Fields cannot be shared across reports

---

### Question 9

**Which of the following is NOT a valid Calculated Field function type in Workday?**

(A) Arithmetic Calculation
(B) SQL Query
(C) Evaluate Expression
(D) Lookup Related Value

---

### Question 10

**What happens if a Calculated Field references a field that is secured by a domain the user does not have access to?**

(A) The entire report fails with an error
(B) The Calculated Field shows the value regardless of security
(C) The Calculated Field returns NULL or blank for that user
(D) Workday prompts the user for elevated permissions

---

## SECTION B: ARITHMETIC CALCULATIONS (Q11-Q18)

---

### Question 11

**You need to calculate a monthly bonus equal to 10% of each worker's total sales. Which Calculated Field function is correct?**

(A) Evaluate Expression
(B) Lookup Related Value
(C) Arithmetic Calculation
(D) Sum Related Instances

---

### Question 12

**An Arithmetic Calculation field requires two inputs: "Total Compensation" and "Hours Worked." The desired output is the hourly rate. Which operation do you configure?**

(A) Total Compensation + Hours Worked
(B) Total Compensation * Hours Worked
(C) Total Compensation - Hours Worked
(D) Total Compensation / Hours Worked

---

### Question 13

**Can an Arithmetic Calculation function accept a text field directly as an input?**

(A) Yes, Workday automatically converts text to numbers
(B) Yes, but only if the text contains only digits
(C) No -- Arithmetic Calculations only work with date fields
(D) No -- the text field must first be converted to a numeric value using a conversion function

---

### Question 14

**A report needs to display each worker's annual pay multiplied by 2 for insurance coverage calculation purposes. Which approach is correct?**

(A) Create an Evaluate Expression with a condition check
(B) Create a Concatenate Text field combining pay and a multiplier
(C) Create an Arithmetic Calculation: Annual Pay * 2
(D) Create a Lookup Related Value to find the insurance field

---

### Question 15

**What is the result type of an Arithmetic Calculation Calculated Field?**

(A) Always text
(B) Always a date
(C) Depends on the input types
(D) Always numeric

---

### Question 16

**You need to calculate a prorated salary for a worker who started mid-month. The formula is: (Annual Salary / 365) * Days Worked in First Month. How many Arithmetic Calculation steps are needed?**

(A) One -- you can nest the entire formula in a single Arithmetic Calculation
(B) Three -- one for each operation
(C) Arithmetic Calculations cannot handle this; use Evaluate Expression
(D) Two -- one for the daily rate (Annual Salary / 365) and one for the proration (Daily Rate * Days Worked)

---

### Question 17

**An Arithmetic Calculation divides "Total Bonus Pool" by "Number of Employees." If "Number of Employees" is zero for a particular organisation, what happens?**

(A) The result is zero
(B) The result is infinity
(C) The result is NULL/blank or an error depending on configuration
(D) Workday automatically substitutes 1 for zero

---

### Question 18

**What is the recommended approach to handle potential division-by-zero in an Arithmetic Calculation?**

(A) Ignore it; Workday handles it automatically
(B) Use a Lookup Related Value instead
(C) Wrap the Arithmetic Calculation inside an Evaluate Expression that checks if the denominator is zero before dividing
(D) Convert the denominator to text first

---

## SECTION C: DATE FUNCTIONS (Q19-Q27)

---

### Question 19

**An HR department needs a field that calculates an employee's probation end date (90 days after hire date). Which function should be used?**

(A) Date Difference
(B) Increment or Decrement Date
(C) Build Date
(D) Date Constant

---

### Question 20

**What does the "Date Difference" Calculated Field function return?**

(A) A new date
(B) A text representation of a date
(C) The numeric difference between two dates in a specified unit (days, months, years)
(D) A Boolean (true/false)

---

### Question 21

**To calculate an employee's tenure in years (Current Date minus Hire Date), which function is correct?**

(A) Increment or Decrement Date
(B) Arithmetic Calculation
(C) Date Difference (in years)
(D) Concatenate Text

---

### Question 22

**What does the "Build Date" function do?**

(A) Calculates the difference between two dates
(B) Adds days to an existing date
(C) Converts a date to text
(D) Constructs a date value from separate year, month, and day components

---

### Question 23

**What does the "Date Constant" function provide?**

(A) A calculated date based on another date field
(B) The difference between two dates
(C) A fixed, hard-coded date value that does not change (e.g., a specific policy effective date)
(D) Today's date

---

### Question 24

**You need a Calculated Field that returns the date six months BEFORE an employee's termination date. Which function and configuration do you use?**

(A) Increment or Decrement Date with +6 months
(B) Date Difference with 6 months
(C) Build Date with the termination month minus 6
(D) Increment or Decrement Date with -6 months

---

### Question 25

**An employee's benefits eligibility date is the first day of the month following their hire date. Which combination of functions would you MOST LIKELY use?**

(A) Arithmetic Calculation only
(B) Date Constant
(C) Increment or Decrement Date (add 1 month) combined with Build Date (to set the day to 1)
(D) Concatenate Text

---

### Question 26

**The "Lookup Value as of Date" Calculated Field has which two date options?**

(A) Start Date and End Date
(B) Hire Date and Termination Date
(C) Current Date and Future Date
(D) Effective Date and Entry Date

---

### Question 27

**A compliance report needs to flag employees whose last performance review was more than 365 days ago. Which Calculated Field approach is correct?**

(A) Use Arithmetic Calculation on the review date
(B) Use Date Difference (Current Date minus Last Review Date), then use Evaluate Expression to check if the result is greater than 365
(C) Use Concatenate Text to display the date difference
(D) Use Increment or Decrement Date to add 365 days to the review date

---

## SECTION D: TEXT FUNCTIONS (Q28-Q34)

---

### Question 28

**You need to display a worker's full name as "Last Name, First Name" in a report. Which function is correct?**

(A) Arithmetic Calculation
(B) Lookup Related Value
(C) Evaluate Expression
(D) Concatenate Text

---

### Question 29

**The "Concatenate Text" function can combine which types of inputs?**

(A) Only text fields
(B) Only numeric fields converted to text
(C) Text fields, text constants (literals), and the text output of other Calculated Fields
(D) Only two inputs at a time

---

### Question 30

**You need to extract the first three characters of an employee's last name for a report code. Which function should you use?**

(A) Concatenate Text
(B) Arithmetic Calculation
(C) Substring Text
(D) Evaluate Expression

---

### Question 31

**A report requires displaying "EXEMPT" or "NON-EXEMPT" based on an employee's FLSA status code. The status code is a text field containing "E" or "N". Which function is correct?**

(A) Concatenate Text
(B) Substring Text
(C) Arithmetic Calculation
(D) Evaluate Expression

---

### Question 32

**You need to convert a numeric employee ID field to text for concatenation with a department code. How should you approach this?**

(A) Use Concatenate Text directly on the numeric field
(B) Use Arithmetic Calculation to combine them
(C) First convert the numeric field to text using a number-to-text conversion function, then use Concatenate Text
(D) Use Lookup Related Value

---

### Question 33

**A report needs to display a worker's email address in uppercase. Which approach is correct?**

(A) Use Concatenate Text with uppercase constants
(B) Use Arithmetic Calculation
(C) Use a text case conversion function (e.g., Upper Case) on the email field
(D) Use Evaluate Expression to check each character

---

### Question 34

**You want to display "Active" if a worker's status field is "A", "On Leave" if "L", and "Terminated" if "T". How many conditions does the Evaluate Expression need?**

(A) One condition
(B) Three conditions
(C) Two conditions and a default (ELSE)
(D) Three conditions and a default (ELSE)

---

## SECTION E: EVALUATE EXPRESSION / CONDITIONAL LOGIC (Q35-Q42)

---

### Question 35

**What is the primary purpose of the "Evaluate Expression" function?**

(A) Performing arithmetic calculations
(B) Looking up values in related objects
(C) Implementing conditional logic (IF/THEN/ELSE)
(D) Concatenating text strings

---

### Question 36

**In an Evaluate Expression, how are multiple conditions evaluated?**

(A) All conditions are evaluated simultaneously
(B) Only the last condition is evaluated
(C) Conditions are evaluated from bottom to top
(D) Conditions are evaluated from top to bottom; the first TRUE condition determines the result

---

### Question 37

**You are building an Evaluate Expression to categorise workers into tenure buckets: "New" (0-1 years), "Mid" (2-5 years), "Senior" (6+ years). What inputs does this Calculated Field require?**

(A) Only the worker's name
(B) The worker's job title
(C) A Date Difference Calculated Field that returns tenure in years
(D) The worker's compensation data

---

### Question 38

**Can an Evaluate Expression return different data types (e.g., text in one branch and a number in another)?**

(A) Yes, each branch can return any type
(B) Yes, but only text and dates
(C) No -- all branches must return the same data type
(D) No -- Evaluate Expression can only return Boolean values

---

### Question 39

**You need a Calculated Field that returns TRUE if a worker is both active AND a manager. Which function is correct?**

(A) Arithmetic Calculation
(B) Concatenate Text
(C) Lookup Related Value
(D) Evaluate Expression with a Boolean AND condition

---

### Question 40

**An Evaluate Expression checks: IF Country = "US" THEN "Domestic" ELSE IF Country = "CA" THEN "Canada" ELSE "International." A worker's country is "CA." What is the result?**

(A) "Domestic"
(B) "International"
(C) "Canada"
(D) NULL

---

### Question 41

**You need a Calculated Field that returns "Eligible" if an employee has 5+ years of tenure AND a performance rating of "Exceeds Expectations" or "Outstanding." How should you structure this?**

(A) Use a single Arithmetic Calculation
(B) Use two separate Concatenate Text fields
(C) Use an Evaluate Expression with the condition: IF (Tenure >= 5) AND (Rating = "Exceeds Expectations" OR Rating = "Outstanding") THEN "Eligible" ELSE "Not Eligible"
(D) Use Lookup Related Value

---

### Question 42

**What is the ELSE clause in an Evaluate Expression?**

(A) An optional clause that is ignored if no conditions match
(B) A clause that overrides all IF conditions
(C) A clause that triggers an error
(D) A mandatory default value returned when none of the IF conditions evaluate to TRUE

---

## SECTION F: LOOKUP FUNCTIONS (Q43-Q50)

---

### Question 43

**What is the purpose of the "Lookup Related Value" function?**

(A) To perform arithmetic on related data
(B) To count instances of a related object
(C) To retrieve a field value from a related business object
(D) To concatenate fields from multiple objects

---

### Question 44

**A report is based on the "Position" business object. You need to display the worker's email address. Which function do you use?**

(A) Concatenate Text
(B) Lookup Related Value (Position -> Worker -> Email Address)
(C) Arithmetic Calculation
(D) Evaluate Expression

---

### Question 45

**What does "Lookup Hierarchy Rollup" enable in a matrix report?**

(A) Arithmetic calculations across hierarchy levels
(B) Security restrictions based on hierarchy
(C) Drillable hierarchy navigation, allowing users to expand from top-level organisations down to individual records
(D) Text concatenation of hierarchy names

---

### Question 46

**Where must the "Lookup Hierarchy Rollup" Calculated Field be placed in a matrix report definition?**

(A) In the Columns grid
(B) In the Rows grid
(C) In the Filters section
(D) In the Drillable Fields grid

---

### Question 47

**You need to display the name of the manager's manager (two levels up) for each worker. How should you configure this?**

(A) Use a single Lookup Related Value
(B) Use Sum Related Instances
(C) Chain two Lookup Related Value fields: first to get the manager, then another to get the manager's manager
(D) Use Concatenate Text

---

### Question 48

**What is "Extract Single Instance" used for?**

(A) Extracting a single numeric value from a text field
(B) Extracting the first character of a text field
(C) Removing duplicate instances from a report
(D) Retrieving one specific instance from a multi-instance related business object based on defined criteria

---

### Question 49

**A report needs to show the value of an employee's base pay as of a specific historical date (e.g., January 1 of the current year), not the current value. Which function should you use?**

(A) Lookup Related Value
(B) Date Difference
(C) Arithmetic Calculation
(D) Lookup Value as of Date, configured with the Effective Date option

---

### Question 50

**What is the difference between "Effective Date" and "Entry Date" options in the "Lookup Value as of Date" function?**

(A) They are the same
(B) Effective Date is for future dates; Entry Date is for past dates
(C) Effective Date returns the value as of the business-effective date (when the change took effect); Entry Date returns the value as of the system-entry date (when the change was entered into Workday)
(D) Effective Date is for compensation; Entry Date is for job changes

---

## SECTION G: AGGREGATION AND MULTI-INSTANCE (Q51-Q56)

---

### Question 51

**A finance report needs to show the total expense amount across all expense lines for each worker. Which function is correct?**

(A) Lookup Related Value
(B) Sum Related Instances
(C) Count Related Instances
(D) Extract Single Instance

---

### Question 52

**What is the difference between "Sum Related Instances" and "Count Related Instances"?**

(A) They are the same
(B) Sum works on text; Count works on numbers
(C) Sum aggregates a numeric field (totals values); Count returns the number of instances (how many records exist)
(D) Sum counts unique values; Count counts all values

---

### Question 53

**You need to count the number of direct reports for each manager. The report is based on the Worker business object. Which function do you use?**

(A) Arithmetic Calculation
(B) Evaluate Expression
(C) Lookup Related Value
(D) Count Related Instances (on the Direct Reports relationship)

---

### Question 54

**Sum Related Instances can be configured with a filter to aggregate only specific instances. True or False?**

(A) True -- you can apply a filter condition to aggregate only instances that meet specific criteria
(B) False -- Sum Related Instances always aggregates all instances without filtering

---

### Question 55

**A report needs the average salary of all workers in each supervisory organisation. Which approach is correct?**

(A) Use a single Concatenate Text field
(B) Use Date Difference
(C) Use Extract Single Instance
(D) Use Arithmetic Calculation: Total Salary / Number of Workers, where Total Salary uses Sum Related Instances and Number of Workers uses Count Related Instances

---

### Question 56

**What does "Extract Multi-Instance" return?**

(A) A single value from one related instance
(B) A count of instances
(C) Multiple values across all matching instances, typically as a multi-valued result for reporting or further processing
(D) An average of numeric values across instances

---

## SECTION H: ADVANCED SCENARIOS AND PERFORMANCE (Q57-Q60)

---

### Question 57

**Scenario: A compensation report includes 15 Calculated Fields, and the report takes over 60 seconds to run. A colleague suggests converting some system-wide Calculated Fields to report-specific fields. Will this improve performance?**

(A) Yes -- report-specific fields are always faster
(B) Yes -- but only if there are more than 20 fields
(C) No -- system-wide fields are always faster
(D) No -- there is no performance difference between system-wide and report-specific Calculated Fields; the issue lies in the number and complexity of the calculations themselves

---

### Question 58

**Scenario: You created an Evaluate Expression with 12 nested conditions for a complex classification. The report runs slowly. What is the MOST effective optimisation?**

(A) Convert the Evaluate Expression to 12 separate Arithmetic Calculations
(B) Add more conditions to make the evaluation faster
(C) Reduce the number of conditions by grouping similar categories, or move the classification to a Custom Report Data Source that pre-computes the value
(D) Convert to Concatenate Text

---

### Question 59

**Scenario: An HR analyst requests a report showing each employee's tenure category ("0-1 years", "2-5 years", "6-10 years", "10+ years"), their manager's name, total compensation (base + bonus), and whether they are benefits-eligible (must be full-time AND have 1+ year of tenure). How many Calculated Fields do you need at minimum?**

(A) 2
(B) 7
(C) 5
(D) 4

---

### Question 60

**Scenario: A security administrator reports that a Calculated Field displaying "Annual Bonus" data shows values for some users but returns blank for others, even though all users have access to the report. The Calculated Field uses Lookup Related Value to retrieve the bonus from the Compensation business object. What is the MOST LIKELY cause, and how should it be resolved?**

(A) The Calculated Field has a bug; rebuild it from scratch
(B) The report has a filter excluding certain users
(C) Lookup Related Value cannot retrieve compensation data
(D) The users who see blanks do not have domain security access to the Compensation domain; grant View access to the Compensation domain for the appropriate security groups

---
---

# ANSWER KEY WITH EXPLANATIONS

---

### Q1 -- Answer: C

A **Calculated Field** is a custom field that derives or transforms data **at runtime** using existing fields and functions. It is NOT stored in the database -- it is computed each time it is referenced.

---

### Q2 -- Answer: D

Every Calculated Field is associated with a **business object**. The business object determines which fields and related objects are available as inputs.

---

### Q3 -- Answer: B

Calculated Fields can be used in **reports, integrations, business processes, condition rules, security configurations, and other configurable areas** within Workday.

---

### Q4 -- Answer: D

**System-wide** Calculated Fields are created using "Create Calculated Field" and are reusable across the tenant. **Report-specific** fields are created within a report and exist only in that report. System-wide fields are preferred for reusability.

---

### Q5 -- Answer: C

Calculated Fields are evaluated **at runtime** -- each time they are referenced. There is no pre-computation or caching.

---

### Q6 -- Answer: C

The **"Create Calculated Field"** task creates system-wide Calculated Fields, letting you select the business object, function type, and inputs.

---

### Q7 -- Answer: D

A Calculated Field on the Worker business object can access **fields on the Worker object AND its related business objects** (e.g., Position, Supervisory Organisation, Compensation).

---

### Q8 -- Answer: C

A Calculated Field on "Worker" is not directly available on a "Position"-based report UNLESS Position has a **related object relationship** to Worker. If so, it can be accessed through the chain.

---

### Q9 -- Answer: B

**SQL Query** is NOT valid. Workday does not expose SQL access. Valid types include Arithmetic Calculation, Evaluate Expression, Lookup Related Value, Concatenate Text, Sum Related Instances, and others.

---

### Q10 -- Answer: C

Workday enforces **domain security at the field level**. If a user lacks access to a secured domain, the Calculated Field returns **NULL/blank** for that user. The rest of the report renders normally.

---

### Q11 -- Answer: C

**Arithmetic Calculation** is designed for mathematical operations. To compute 10% of sales, multiply the sales field by 0.10.

---

### Q12 -- Answer: D

Hourly rate = Total Compensation **divided by** Hours Worked. Division is a core operation of Arithmetic Calculation.

---

### Q13 -- Answer: D

Arithmetic Calculation requires **numeric inputs**. Text fields must first be converted to a number using a **text-to-number conversion function**.

---

### Q14 -- Answer: C

Straightforward multiplication: Annual Pay * 2. **Arithmetic Calculation** is the correct function for any math operation.

---

### Q15 -- Answer: D

Arithmetic Calculation always returns a **numeric** result, regardless of the operation.

---

### Q16 -- Answer: D

Workday's Arithmetic Calculation typically handles one operation at a time. Create **two Calculated Fields**: first for daily rate (Annual Salary / 365), second for proration (Daily Rate * Days Worked).

---

### Q17 -- Answer: C

Division by zero typically returns **NULL/blank or triggers a runtime error**. Best practice is to use an Evaluate Expression wrapper that checks for zero first.

---

### Q18 -- Answer: C

Create an **Evaluate Expression**: IF denominator = 0 THEN return 0 (or default) ELSE perform the Arithmetic Calculation. This prevents runtime errors.

---

### Q19 -- Answer: B

**Increment or Decrement Date** adds a specified number of days, months, or years to a date. Adding 90 days to hire date gives the probation end date.

---

### Q20 -- Answer: C

**Date Difference** returns a **numeric value** representing the difference between two dates in the specified unit (days, months, or years). It does NOT return a date.

---

### Q21 -- Answer: C

**Date Difference** with the unit set to "Years" calculates years between the hire date and the current date, directly giving tenure.

---

### Q22 -- Answer: D

**Build Date** constructs a complete date value from separate **year, month, and day** components.

---

### Q23 -- Answer: C

**Date Constant** provides a **fixed, hard-coded date value** that remains the same every time, useful for reference dates.

---

### Q24 -- Answer: D

**Increment or Decrement Date** with **-6 months** subtracts six months from the termination date, giving you the date six months prior.

---

### Q25 -- Answer: C

Use **Increment or Decrement Date** to add one month, then **Build Date** to set the day to 1, producing the first day of the following month.

---

### Q26 -- Answer: D

The function supports **Effective Date** (business-effective date) and **Entry Date** (system-entry/audit date). The distinction matters for point-in-time reporting.

---

### Q27 -- Answer: B

Create a **Date Difference** field (in days) between current date and last review date. Then create an **Evaluate Expression**: IF difference > 365 THEN "Overdue" ELSE "Current."

---

### Q28 -- Answer: D

**Concatenate Text** combines multiple text strings. Concatenate Last Name + ", " + First Name to produce "Last Name, First Name."

---

### Q29 -- Answer: C

Concatenate Text can combine **text fields, text constants (literal strings), and the text output of other Calculated Fields**. It supports multiple inputs.

---

### Q30 -- Answer: C

**Substring Text** extracts a specified portion of a text string. Configure start position as 1 and length as 3 for the first three characters.

---

### Q31 -- Answer: D

This is conditional logic: IF status = "E" THEN "EXEMPT" ELSE "NON-EXEMPT." **Evaluate Expression** handles IF/THEN/ELSE logic.

---

### Q32 -- Answer: C

Concatenate Text requires **text inputs**. A numeric field must be **converted to text** first using the appropriate conversion function.

---

### Q33 -- Answer: C

Workday provides text manipulation functions including **Upper Case** for converting text to uppercase. Apply it to the email field.

---

### Q34 -- Answer: C

You need: IF "A" THEN "Active"; ELSE IF "L" THEN "On Leave"; ELSE "Terminated." This is **two explicit conditions** plus a **default ELSE** -- the most efficient design.

---

### Q35 -- Answer: C

**Evaluate Expression** is Workday's conditional logic function for IF/THEN/ELSE statements. It is the equivalent of an IF statement in spreadsheets.

---

### Q36 -- Answer: D

Conditions are evaluated **sequentially from top to bottom**. The first TRUE condition determines the result; no further conditions are checked.

---

### Q37 -- Answer: C

The Evaluate Expression needs a **numeric tenure value** from a separate **Date Difference Calculated Field** (Current Date minus Hire Date in years).

---

### Q38 -- Answer: C

All branches must return the **same data type**. Mixing types (e.g., a number in one branch and text in another) produces an error.

---

### Q39 -- Answer: D

**Evaluate Expression** supports Boolean logic including **AND** conditions: IF (Active) AND (Is Manager) THEN TRUE ELSE FALSE.

---

### Q40 -- Answer: C

Evaluated top to bottom: Country = "US" is FALSE; Country = "CA" is TRUE. Result is **"Canada."** The ELSE is never reached.

---

### Q41 -- Answer: C

This requires **conditional logic combining AND and OR operators** in an Evaluate Expression to check compound conditions for eligibility.

---

### Q42 -- Answer: D

The ELSE clause provides a **mandatory default value** returned when none of the IF conditions match. Best practice is to always include an ELSE.

---

### Q43 -- Answer: C

**Lookup Related Value (LRV)** retrieves a specific field value from a **related business object** by traversing relationship chains.

---

### Q44 -- Answer: B

Since the data source is Position, use **Lookup Related Value** to traverse: Position -> Worker -> Email Address.

---

### Q45 -- Answer: C

**Lookup Hierarchy Rollup** enables **drillable hierarchies** in matrix reports, allowing expansion from top-level orgs down to individual records.

---

### Q46 -- Answer: D

The field must be placed in the **Drillable Fields grid** to activate hierarchy navigation. Rows or Columns placement does not enable drill-down.

---

### Q47 -- Answer: C

**Chain two** Lookup Related Value fields: first to get the manager, then another to get the manager's manager for two-level traversal.

---

### Q48 -- Answer: D

**Extract Single Instance** retrieves **one specific record** from a multi-instance related business object based on defined criteria (e.g., the primary address).

---

### Q49 -- Answer: D

**Lookup Value as of Date** with the **Effective Date** option retrieves the value as it was on a specific historical date for point-in-time reporting.

---

### Q50 -- Answer: C

**Effective Date** = when the change **took business effect**. **Entry Date** = when the change **was entered into the system**. These can differ significantly.

---

### Q51 -- Answer: B

**Sum Related Instances** aggregates a numeric field across all instances of a related multi-instance object, returning the total.

---

### Q52 -- Answer: C

**Sum** adds up a numeric field (totals values). **Count** returns the number of related instances (how many records exist).

---

### Q53 -- Answer: D

**Count Related Instances** on the Direct Reports relationship returns the number of workers reporting to each manager.

---

### Q54 -- Answer: A

**True** -- Sum Related Instances supports filtering to aggregate only instances that meet specified criteria (e.g., only "Approved" expenses).

---

### Q55 -- Answer: D

Average = Total / Count. Use **Sum Related Instances** for total salary, **Count Related Instances** for worker count, then **Arithmetic Calculation** to divide.

---

### Q56 -- Answer: C

**Extract Multi-Instance** returns multiple values as a multi-valued result, unlike Extract Single Instance (one value) or Sum/Count (single aggregate).

---

### Q57 -- Answer: D

There is **no inherent performance difference** between system-wide and report-specific fields. Performance depends on the **number, complexity, and relationship joins** of the calculations.

---

### Q58 -- Answer: C

Simplify by **grouping similar categories** or moving the classification to a **Custom Report Data Source (CRDS)** where the value is pre-computed and indexed.

---

### Q59 -- Answer: D

Minimum **4** fields: (1) Date Difference for tenure, (2) Evaluate Expression for tenure category, (3) Arithmetic Calculation for total compensation, (4) Evaluate Expression for benefits eligibility. Manager's name may be a standard field.

---

### Q60 -- Answer: D

Workday enforces **domain security** even within Calculated Fields. Users without **View access** to the Compensation domain see NULL/blank. Grant access and **activate** pending security changes.

---

# QUICK-REFERENCE ANSWER KEY

| Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | C | 11 | C | 21 | C | 31 | D | 41 | C | 51 | B |
| 2 | D | 12 | D | 22 | D | 32 | C | 42 | D | 52 | C |
| 3 | B | 13 | D | 23 | C | 33 | C | 43 | C | 53 | D |
| 4 | D | 14 | C | 24 | D | 34 | C | 44 | B | 54 | A |
| 5 | C | 15 | D | 25 | C | 35 | C | 45 | C | 55 | D |
| 6 | C | 16 | D | 26 | D | 36 | D | 46 | D | 56 | C |
| 7 | D | 17 | C | 27 | B | 37 | C | 47 | C | 57 | D |
| 8 | C | 18 | C | 28 | D | 38 | C | 48 | D | 58 | C |
| 9 | B | 19 | B | 29 | C | 39 | D | 49 | D | 59 | D |
| 10 | C | 20 | C | 30 | C | 40 | C | 50 | C | 60 | D |

---

# FUNCTION REFERENCE CHEAT SHEET

| Function | Purpose | Return Type |
|---|---|---|
| **Arithmetic Calculation** | Math operations (+, -, *, /) | Numeric |
| **Evaluate Expression** | Conditional logic (IF/THEN/ELSE) | Any (must be consistent) |
| **Lookup Related Value** | Retrieve field from related business object | Matches source field type |
| **Lookup Hierarchy Rollup** | Enable drill-down hierarchies in matrix reports | Hierarchy node |
| **Lookup Value as of Date** | Point-in-time field retrieval | Matches source field type |
| **Concatenate Text** | Combine multiple text strings | Text |
| **Substring Text** | Extract portion of text string | Text |
| **Upper Case / Lower Case** | Change text case | Text |
| **Increment or Decrement Date** | Add/subtract time from a date | Date |
| **Date Difference** | Numeric difference between two dates | Numeric |
| **Build Date** | Construct date from components | Date |
| **Date Constant** | Fixed hard-coded date value | Date |
| **Sum Related Instances** | Sum numeric field across related records | Numeric |
| **Count Related Instances** | Count number of related records | Numeric |
| **Extract Single Instance** | Retrieve one record from multi-instance | Matches source type |
| **Extract Multi-Instance** | Retrieve all matching records from multi-instance | Multi-valued |

---

*End of Calculated Fields Mock Examination -- 60 Questions*
