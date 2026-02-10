# WORKDAY PRO HCM REPORTING -- CALCULATED FIELDS EXAMINATION

## 60 Exam-Ready Questions with Answers and Explanations

**Exam Code:** Workday-Pro-HCM-Reporting
**Topic Focus:** Calculated Fields (~25% of Exam Weightage)
**Print Format:** Black-and-White, A4-Optimised

---

> **Prepared by:** Senior Chief Examiner, Workday Reporting Certification
>
> These 60 questions cover every testable area of Calculated Fields: core
> functions, date operations, text manipulation, conditional logic, lookups,
> aggregation, hierarchy rollups, usage contexts, performance, and
> scenario-based application. Questions are ordered from foundational to
> advanced.

---

## TABLE OF CONTENTS

- Section A: Fundamentals and Concepts (Q1-Q10)
- Section B: Arithmetic Calculations (Q11-Q18)
- Section C: Date Functions (Q19-Q27)
- Section D: Text Functions (Q28-Q34)
- Section E: Evaluate Expression / Conditional Logic (Q35-Q42)
- Section F: Lookup Functions (Q43-Q50)
- Section G: Aggregation and Multi-Instance (Q51-Q56)
- Section H: Advanced Scenarios and Performance (Q57-Q60)

---
---

# SECTION A: FUNDAMENTALS AND CONCEPTS

---

### Question 1

**What is a Calculated Field in Workday?**

(A) A field stored permanently in the Workday database
(B) A custom field that derives or transforms data at runtime using
existing fields and functions
(C) A field that can only be used in integrations
(D) A system field that cannot be modified

**Correct Answer: (B)**

**Explanation:**
A **Calculated Field** is a custom field that derives or transforms data **at
runtime** using existing fields and Workday functions. It is NOT stored in the
database -- it is computed each time it is referenced. Calculated Fields are
fundamental tools for customisation across reports, integrations, and business
processes.

---

### Question 2

**Calculated Fields in Workday are always associated with which of the
following?**

(A) A security group
(B) A business object
(C) A supervisory organisation
(D) A report only

**Correct Answer: (B)**

**Explanation:**
Every Calculated Field is associated with a **business object**. The business
object determines which fields and related objects are available as inputs.
When you create a Calculated Field, you must select the business object it
belongs to, and it can only access fields available on that object or its
related objects.

---

### Question 3

**Where can Calculated Fields be used in Workday? (Select the BEST answer)**

(A) Only in custom reports
(B) Only in integrations
(C) In reports, integrations, business processes, and other configurable areas
(D) Only in business processes

**Correct Answer: (C)**

**Explanation:**
Calculated Fields are versatile and can be used in **reports, integrations,
business processes, condition rules, security configurations, and other
configurable areas** within Workday. They are not confined to a single
functional area.

---

### Question 4

**What is the difference between a system-wide (tenant-level) Calculated
Field and a report-specific Calculated Field?**

(A) There is no difference
(B) A system-wide Calculated Field is created via "Create Calculated Field"
and can be reused across any report or process on the same business object;
a report-specific one is created within a report and is only available in
that report
(C) A report-specific Calculated Field is more performant
(D) A system-wide Calculated Field can only be used in integrations

**Correct Answer: (B)**

**Explanation:**
**System-wide (tenant-level)** Calculated Fields are created using the
"Create Calculated Field" task and are reusable across any report, integration,
or business process that references the same business object. **Report-specific**
Calculated Fields are created directly within a report definition and are
available only within that specific report. System-wide fields are preferred
for reusability.

---

### Question 5

**When is a Calculated Field evaluated?**

(A) When the tenant is loaded
(B) At runtime, each time it is referenced (e.g., when a report is run)
(C) Once per day during a batch job
(D) Only during integration executions

**Correct Answer: (B)**

**Explanation:**
Calculated Fields are evaluated **at runtime** -- each time they are referenced.
When a user runs a report containing a Calculated Field, the system computes
the value at that moment using current data. There is no pre-computation or
caching of Calculated Field values.

---

### Question 6

**Which Workday task is used to create a system-wide Calculated Field?**

(A) Create Custom Report
(B) Create Calculated Field
(C) Maintain Calculated Fields
(D) Build Custom Data Source

**Correct Answer: (B)**

**Explanation:**
The **"Create Calculated Field"** task is used to create system-wide (tenant-
level) Calculated Fields. This task allows you to select the business object,
define the function type, configure inputs, and save the field for reuse across
the tenant.

---

### Question 7

**A Calculated Field created on the "Worker" business object can access
fields from which of the following?**

(A) Only fields directly on the Worker object
(B) Fields on the Worker object and fields on its related business objects
(C) Fields on any business object in the tenant
(D) Only fields on the Worker object's parent object

**Correct Answer: (B)**

**Explanation:**
A Calculated Field on the Worker business object can access **fields directly
on the Worker object AND fields on its related business objects** (e.g.,
Position, Supervisory Organisation, Compensation). It cannot access fields on
unrelated business objects.

---

### Question 8

**You have created a system-wide Calculated Field on the "Worker" business
object. A colleague wants to use it in a report based on the "Position"
business object. Is this possible?**

(A) Yes, directly
(B) No -- the Calculated Field must be on the same business object as the
report's primary data source, or accessible via a related object relationship
(C) Yes, but only if the report is a composite report
(D) No -- Calculated Fields cannot be shared across reports

**Correct Answer: (B)**

**Explanation:**
A Calculated Field created on "Worker" is not directly available on a "Position"
-based report UNLESS the Position business object has a **related object
relationship** to Worker. If such a relationship exists, the field can be
accessed through the relationship chain. Otherwise, the field must be recreated
on the Position business object.

---

### Question 9

**Which of the following is NOT a valid Calculated Field function type
in Workday?**

(A) Arithmetic Calculation
(B) Evaluate Expression
(C) SQL Query
(D) Lookup Related Value

**Correct Answer: (C)**

**Explanation:**
**SQL Query** is NOT a valid Calculated Field function type. Workday does not
expose SQL-level access. Valid function types include Arithmetic Calculation,
Evaluate Expression, Lookup Related Value, Concatenate Text, Sum Related
Instances, Increment or Decrement Date, Date Difference, and others.

---

### Question 10

**What happens if a Calculated Field references a field that is secured
by a domain the user does not have access to?**

(A) The entire report fails with an error
(B) The Calculated Field returns NULL or blank for that user
(C) The Calculated Field shows the value regardless of security
(D) Workday prompts the user for elevated permissions

**Correct Answer: (B)**

**Explanation:**
Workday enforces **domain security at the field level**. If a Calculated Field
references a secured field that the user lacks access to, the Calculated Field
returns **NULL or blank** for that user. The rest of the report continues to
render normally. Security is never bypassed.

---
---

# SECTION B: ARITHMETIC CALCULATIONS

---

### Question 11

**You need to calculate a monthly bonus equal to 10% of each worker's total
sales. Which Calculated Field function is correct?**

(A) Evaluate Expression
(B) Arithmetic Calculation
(C) Lookup Related Value
(D) Sum Related Instances

**Correct Answer: (B)**

**Explanation:**
**Arithmetic Calculation** is designed for mathematical operations: addition,
subtraction, multiplication, and division. To compute 10% of sales, you
multiply the sales field by 0.10. The Workday documentation states:
"Arithmetic Calculation creates a numeric field using mathematical operations
performed on existing fields."

---

### Question 12

**An Arithmetic Calculation field requires two inputs: "Total Compensation"
and "Hours Worked." The desired output is the hourly rate. Which operation
do you configure?**

(A) Total Compensation + Hours Worked
(B) Total Compensation - Hours Worked
(C) Total Compensation / Hours Worked
(D) Total Compensation * Hours Worked

**Correct Answer: (C)**

**Explanation:**
Hourly rate = Total Compensation **divided by** Hours Worked. The Arithmetic
Calculation function supports division as one of its core operations.

---

### Question 13

**Can an Arithmetic Calculation function accept a text field directly as
an input?**

(A) Yes, Workday automatically converts text to numbers
(B) No -- the text field must first be converted to a numeric value using
a conversion function
(C) Yes, but only if the text contains only digits
(D) No -- Arithmetic Calculations only work with date fields

**Correct Answer: (B)**

**Explanation:**
Arithmetic Calculation requires **numeric inputs**. Text fields cannot be used
directly, even if they contain only digits. You must first convert the text
to a number using a **text-to-number conversion function** before using it as
an input to an Arithmetic Calculation.

---

### Question 14

**A report needs to display each worker's annual pay multiplied by 2 for
insurance coverage calculation purposes. Which approach is correct?**

(A) Create an Evaluate Expression with a condition check
(B) Create an Arithmetic Calculation: Annual Pay * 2
(C) Create a Lookup Related Value to find the insurance field
(D) Create a Concatenate Text field combining pay and a multiplier

**Correct Answer: (B)**

**Explanation:**
This is a straightforward multiplication: Annual Pay * 2. **Arithmetic
Calculation** is the correct function. Evaluate Expression is for conditional
logic, Lookup Related Value is for traversing related objects, and Concatenate
Text is for string operations.

---

### Question 15

**What is the result type of an Arithmetic Calculation Calculated Field?**

(A) Always text
(B) Always numeric
(C) Always a date
(D) Depends on the input types

**Correct Answer: (B)**

**Explanation:**
Arithmetic Calculation always returns a **numeric** result, regardless of the
specific operation (addition, subtraction, multiplication, or division).

---

### Question 16

**You need to calculate a prorated salary for a worker who started mid-month.
The formula is: (Annual Salary / 365) * Days Worked in First Month. How many
Arithmetic Calculation steps are needed?**

(A) One -- you can nest the entire formula in a single Arithmetic Calculation
(B) Two -- one for the daily rate (Annual Salary / 365) and one for the
proration (Daily Rate * Days Worked)
(C) Three -- one for each operation
(D) Arithmetic Calculations cannot handle this; use Evaluate Expression

**Correct Answer: (B)**

**Explanation:**
Workday's Arithmetic Calculation typically handles one operation at a time. For
a two-step formula, you create **two Calculated Fields**: the first computes the
daily rate (Annual Salary / 365), and the second multiplies that result by
Days Worked. The second field references the first field as an input.

---

### Question 17

**An Arithmetic Calculation divides "Total Bonus Pool" by "Number of
Employees." If "Number of Employees" is zero for a particular organisation,
what happens?**

(A) The result is zero
(B) The result is NULL/blank or an error depending on configuration
(C) The result is infinity
(D) Workday automatically substitutes 1 for zero

**Correct Answer: (B)**

**Explanation:**
Division by zero in Workday Calculated Fields typically returns **NULL/blank
or triggers a runtime error**. It does NOT return zero or infinity. Best practice
is to use an **Evaluate Expression** wrapper that checks for zero before
performing the division.

---

### Question 18

**What is the recommended approach to handle potential division-by-zero
in an Arithmetic Calculation?**

(A) Ignore it; Workday handles it automatically
(B) Wrap the Arithmetic Calculation inside an Evaluate Expression that
checks if the denominator is zero before dividing
(C) Use a Lookup Related Value instead
(D) Convert the denominator to text first

**Correct Answer: (B)**

**Explanation:**
The recommended approach is to create an **Evaluate Expression** with a
condition: IF denominator = 0 THEN return 0 (or a default value) ELSE
perform the Arithmetic Calculation. This prevents runtime errors and ensures
clean output.

---
---

# SECTION C: DATE FUNCTIONS

---

### Question 19

**An HR department needs a field that calculates an employee's probation
end date (90 days after hire date). Which function should be used?**

(A) Date Difference
(B) Build Date
(C) Increment or Decrement Date
(D) Date Constant

**Correct Answer: (C)**

**Explanation:**
**Increment or Decrement Date** calculates a date that is a specified number
of years, months, days, hours, minutes, seconds, or milliseconds before or
after a given date field. Adding 90 days to the hire date produces the
probation end date.

---

### Question 20

**What does the "Date Difference" Calculated Field function return?**

(A) A new date
(B) The numeric difference between two dates in a specified unit (days,
months, years)
(C) A text representation of a date
(D) A Boolean (true/false)

**Correct Answer: (B)**

**Explanation:**
**Date Difference** returns a **numeric value** representing the difference
between two dates in the unit you specify (days, months, or years). It does
NOT return a date -- it returns a number. This is commonly used to calculate
tenure or age.

---

### Question 21

**To calculate an employee's tenure in years (Current Date minus Hire Date),
which function is correct?**

(A) Increment or Decrement Date
(B) Date Difference (in years)
(C) Arithmetic Calculation
(D) Concatenate Text

**Correct Answer: (B)**

**Explanation:**
**Date Difference** with the unit set to "Years" calculates the number of years
between the hire date and the current date. This directly gives tenure in years.
Arithmetic Calculation cannot operate on dates directly. Increment/Decrement
Date returns a new date, not a numeric tenure value.

---

### Question 22

**What does the "Build Date" function do?**

(A) Calculates the difference between two dates
(B) Constructs a date value from separate year, month, and day components
(C) Adds days to an existing date
(D) Converts a date to text

**Correct Answer: (B)**

**Explanation:**
**Build Date** constructs a complete date value from separate **year, month,
and day** inputs. This is useful when you have individual components (e.g., a
year field and a month field) and need to combine them into a single date.

---

### Question 23

**What does the "Date Constant" function provide?**

(A) A calculated date based on another date field
(B) A fixed, hard-coded date value that does not change (e.g., a specific
policy effective date)
(C) Today's date
(D) The difference between two dates

**Correct Answer: (B)**

**Explanation:**
**Date Constant** provides a **fixed, hard-coded date value** that remains the
same every time the Calculated Field is evaluated. This is useful for reference
dates such as policy start dates, fiscal year start dates, or compliance
deadlines.

---

### Question 24

**You need a Calculated Field that returns the date six months BEFORE an
employee's termination date. Which function and configuration do you use?**

(A) Increment or Decrement Date with +6 months
(B) Increment or Decrement Date with -6 months
(C) Date Difference with 6 months
(D) Build Date with the termination month minus 6

**Correct Answer: (B)**

**Explanation:**
**Increment or Decrement Date** with a **-6 months** parameter subtracts six
months from the termination date, giving you the date six months prior. The
"Decrement" option is specifically for moving backward in time.

---

### Question 25

**An employee's benefits eligibility date is the first day of the month
following their hire date. Which combination of functions would you MOST
LIKELY use?**

(A) Arithmetic Calculation only
(B) Increment or Decrement Date (add 1 month) combined with Build Date
(to set the day to 1)
(C) Date Constant
(D) Concatenate Text

**Correct Answer: (B)**

**Explanation:**
You would first use **Increment or Decrement Date** to add one month to the
hire date. Then use **Build Date** (or equivalent logic) to set the day
component to 1, producing the first day of the following month. This
combination handles the requirement precisely.

---

### Question 26

**The "Lookup Value as of Date" Calculated Field has which two date options?**

(A) Start Date and End Date
(B) Effective Date and Entry Date
(C) Hire Date and Termination Date
(D) Current Date and Future Date

**Correct Answer: (B)**

**Explanation:**
The **"Lookup Value as of Date"** function supports **Effective Date** and
**Entry Date** as its two date options. Effective Date returns the value
as of the business-effective date, while Entry Date returns the value as of
the system-entry (audit) date. The distinction is important for point-in-time
reporting.

---

### Question 27

**A compliance report needs to flag employees whose last performance review
was more than 365 days ago. Which Calculated Field approach is correct?**

(A) Use Date Difference (Current Date minus Last Review Date), then use
Evaluate Expression to check if the result is greater than 365
(B) Use Arithmetic Calculation on the review date
(C) Use Concatenate Text to display the date difference
(D) Use Increment or Decrement Date to add 365 days to the review date

**Correct Answer: (A)**

**Explanation:**
First, create a **Date Difference** field (in days) between the current date
and the last review date. Then, create an **Evaluate Expression** that checks
IF the difference > 365, THEN return "Overdue" ELSE return "Current." This
two-step approach combines date calculation with conditional evaluation.

---
---

# SECTION D: TEXT FUNCTIONS

---

### Question 28

**You need to display a worker's full name as "Last Name, First Name" in
a report. Which function is correct?**

(A) Arithmetic Calculation
(B) Evaluate Expression
(C) Concatenate Text
(D) Lookup Related Value

**Correct Answer: (C)**

**Explanation:**
**Concatenate Text** combines multiple text strings into a single output. You
concatenate the Last Name field, a literal ", " separator, and the First Name
field to produce "Last Name, First Name."

---

### Question 29

**The "Concatenate Text" function can combine which types of inputs?**

(A) Only text fields
(B) Text fields, text constants (literals), and the text output of other
Calculated Fields
(C) Only numeric fields converted to text
(D) Only two inputs at a time

**Correct Answer: (B)**

**Explanation:**
Concatenate Text can combine **text fields, text constants (literal strings
like ", " or " - "), and the text output of other Calculated Fields**. It
supports multiple inputs, not just two.

---

### Question 30

**You need to extract the first three characters of an employee's last name
for a report code. Which function should you use?**

(A) Concatenate Text
(B) Substring Text
(C) Arithmetic Calculation
(D) Evaluate Expression

**Correct Answer: (B)**

**Explanation:**
**Substring Text** extracts a specified portion of a text string based on
start position and length. To get the first three characters, configure the
start position as 1 and the length as 3.

---

### Question 31

**A report requires displaying "EXEMPT" or "NON-EXEMPT" based on an
employee's FLSA status code. The status code is a text field containing
"E" or "N". Which function is correct?**

(A) Concatenate Text
(B) Evaluate Expression
(C) Substring Text
(D) Arithmetic Calculation

**Correct Answer: (B)**

**Explanation:**
This is a conditional logic scenario: IF status = "E" THEN "EXEMPT" ELSE
"NON-EXEMPT." The **Evaluate Expression** function handles conditional
(if/then/else) logic. Concatenate Text only joins strings without conditions.

---

### Question 32

**You need to convert a numeric employee ID field to text for concatenation
with a department code. How should you approach this?**

(A) Use Concatenate Text directly on the numeric field
(B) First convert the numeric field to text using a number-to-text conversion
function, then use Concatenate Text
(C) Use Arithmetic Calculation to combine them
(D) Use Lookup Related Value

**Correct Answer: (B)**

**Explanation:**
Concatenate Text operates on **text inputs**. A numeric field must be
**converted to text** first using the appropriate conversion function before
it can be used as an input to Concatenate Text.

---

### Question 33

**A report needs to display a worker's email address in uppercase. Which
approach is correct?**

(A) Use Concatenate Text with uppercase constants
(B) Use a text case conversion function (e.g., Upper Case) on the email field
(C) Use Arithmetic Calculation
(D) Use Evaluate Expression to check each character

**Correct Answer: (B)**

**Explanation:**
Workday provides text manipulation functions including **Upper Case** for
converting text to uppercase. Applying this function to the email field
produces the entire address in uppercase. Concatenate Text does not change
case; it only joins strings.

---

### Question 34

**You want to display "Active" if a worker's status field is "A", "On Leave"
if "L", and "Terminated" if "T". How many conditions does the Evaluate
Expression need?**

(A) One condition
(B) Two conditions and a default (ELSE)
(C) Three conditions
(D) Three conditions and a default (ELSE)

**Correct Answer: (B)**

**Explanation:**
The Evaluate Expression evaluates conditions **top to bottom** until the first
match. You need: IF status = "A" THEN "Active"; ELSE IF status = "L" THEN
"On Leave"; ELSE "Terminated." This is **two explicit conditions** with a
**default ELSE** for "T" (and any other unexpected value). While three
conditions would also work, the most efficient design uses two conditions
plus a default.

---
---

# SECTION E: EVALUATE EXPRESSION / CONDITIONAL LOGIC

---

### Question 35

**What is the primary purpose of the "Evaluate Expression" function?**

(A) Performing arithmetic calculations
(B) Implementing conditional logic (IF/THEN/ELSE)
(C) Concatenating text strings
(D) Looking up values in related objects

**Correct Answer: (B)**

**Explanation:**
**Evaluate Expression** is Workday's conditional logic function. It evaluates a
series of conditions (IF/THEN/ELSE) from top to bottom and returns the result
of the first matching condition. It is the equivalent of an IF statement in
spreadsheet formulas.

---

### Question 36

**In an Evaluate Expression, how are multiple conditions evaluated?**

(A) All conditions are evaluated simultaneously
(B) Conditions are evaluated from top to bottom; the first TRUE condition
determines the result
(C) Conditions are evaluated from bottom to top
(D) Only the last condition is evaluated

**Correct Answer: (B)**

**Explanation:**
Conditions in an Evaluate Expression are evaluated **sequentially from top
to bottom**. The moment a condition evaluates to TRUE, its associated THEN
value is returned and no further conditions are evaluated. Order matters.

---

### Question 37

**You are building an Evaluate Expression to categorise workers into tenure
buckets: "New" (0-1 years), "Mid" (2-5 years), "Senior" (6+ years). What
inputs does this Calculated Field require?**

(A) Only the worker's name
(B) A Date Difference Calculated Field that returns tenure in years
(C) The worker's job title
(D) The worker's compensation data

**Correct Answer: (B)**

**Explanation:**
The Evaluate Expression needs a **numeric tenure value** to compare against
the bucket boundaries. This is provided by a separate **Date Difference
Calculated Field** that returns years of service (Current Date minus Hire Date).
The Evaluate Expression then checks: IF tenure <= 1 THEN "New"; ELSE IF
tenure <= 5 THEN "Mid"; ELSE "Senior."

---

### Question 38

**Can an Evaluate Expression return different data types (e.g., text in
one branch and a number in another)?**

(A) Yes, each branch can return any type
(B) No -- all branches must return the same data type
(C) Yes, but only text and dates
(D) No -- Evaluate Expression can only return Boolean values

**Correct Answer: (B)**

**Explanation:**
All branches (THEN and ELSE values) in an Evaluate Expression must return
the **same data type**. If one branch returns text, all branches must return
text. Mixing types (e.g., a number in one branch and text in another)
produces an error.

---

### Question 39

**You need a Calculated Field that returns TRUE if a worker is both active
AND a manager. Which function is correct?**

(A) Arithmetic Calculation
(B) Evaluate Expression with a Boolean AND condition
(C) Concatenate Text
(D) Lookup Related Value

**Correct Answer: (B)**

**Explanation:**
**Evaluate Expression** supports Boolean logic including **AND** conditions. The
configuration is: IF (Worker Status = Active) AND (Is Manager = True) THEN
TRUE ELSE FALSE. This returns a Boolean result based on multiple criteria.

---

### Question 40

**An Evaluate Expression checks: IF Country = "US" THEN "Domestic" ELSE
IF Country = "CA" THEN "Canada" ELSE "International." A worker's country
is "CA." What is the result?**

(A) "Domestic"
(B) "Canada"
(C) "International"
(D) NULL

**Correct Answer: (B)**

**Explanation:**
The conditions are evaluated top to bottom. The first condition (Country = "US")
is FALSE, so it moves to the second (Country = "CA"), which is TRUE. The result
is **"Canada."** The ELSE "International" is never reached.

---

### Question 41

**You need a Calculated Field that returns "Eligible" if an employee has
5+ years of tenure AND a performance rating of "Exceeds Expectations"
or "Outstanding." How should you structure this?**

(A) Use a single Arithmetic Calculation
(B) Use an Evaluate Expression with the condition: IF (Tenure >= 5) AND
(Rating = "Exceeds Expectations" OR Rating = "Outstanding") THEN "Eligible"
ELSE "Not Eligible"
(C) Use two separate Concatenate Text fields
(D) Use Lookup Related Value

**Correct Answer: (B)**

**Explanation:**
This requires **conditional logic combining AND and OR operators**. The Evaluate
Expression checks the compound condition: tenure must be >= 5 AND the rating
must be one of two acceptable values. This is a textbook use case for Evaluate
Expression with Boolean operators.

---

### Question 42

**What is the ELSE clause in an Evaluate Expression?**

(A) An optional clause that is ignored if no conditions match
(B) A mandatory default value returned when none of the IF conditions
evaluate to TRUE
(C) A clause that overrides all IF conditions
(D) A clause that triggers an error

**Correct Answer: (B)**

**Explanation:**
The ELSE clause provides a **default value** returned when none of the explicit
IF conditions match. While Workday may allow you to omit it (returning NULL),
best practice is to always include an ELSE to ensure every scenario produces
a defined result.

---
---

# SECTION F: LOOKUP FUNCTIONS

---

### Question 43

**What is the purpose of the "Lookup Related Value" function?**

(A) To perform arithmetic on related data
(B) To retrieve a field value from a related business object
(C) To count instances of a related object
(D) To concatenate fields from multiple objects

**Correct Answer: (B)**

**Explanation:**
**Lookup Related Value (LRV)** retrieves a specific field value from a **related
business object**. For example, if your report is based on the Worker object,
LRV can traverse the relationship to the Position object and retrieve the
position title, or to the Supervisory Organisation and retrieve the org name.

---

### Question 44

**A report is based on the "Position" business object. You need to display
the worker's email address. Which function do you use?**

(A) Concatenate Text
(B) Arithmetic Calculation
(C) Lookup Related Value (Position -> Worker -> Email Address)
(D) Evaluate Expression

**Correct Answer: (C)**

**Explanation:**
Since the primary data source is Position, the email address is on the related
Worker object. **Lookup Related Value** traverses the relationship chain:
Position -> Worker -> Email Address. This is the standard method for accessing
fields on related objects.

---

### Question 45

**What does "Lookup Hierarchy Rollup" enable in a matrix report?**

(A) Arithmetic calculations across hierarchy levels
(B) Drillable hierarchy navigation, allowing users to expand from top-level
organisations down to individual records
(C) Security restrictions based on hierarchy
(D) Text concatenation of hierarchy names

**Correct Answer: (B)**

**Explanation:**
**Lookup Hierarchy Rollup** enables **drillable hierarchies** in matrix reports.
Users can start at the top-level supervisory organisation and expand
(drill down) through intermediate levels to view data at each tier. Without
this function, matrix reports show flat data without hierarchical navigation.

---

### Question 46

**Where must the "Lookup Hierarchy Rollup" Calculated Field be placed in
a matrix report definition?**

(A) In the Columns grid
(B) In the Rows grid
(C) In the Drillable Fields grid
(D) In the Filters section

**Correct Answer: (C)**

**Explanation:**
The Lookup Hierarchy Rollup field must be included in the **Drillable Fields
grid** of the matrix report definition. This is what enables the drill-down
behaviour. Placing it in Rows or Columns does not activate the hierarchy
navigation feature.

---

### Question 47

**You need to display the name of the manager's manager (two levels up)
for each worker. How should you configure this?**

(A) Use a single Lookup Related Value
(B) Chain two Lookup Related Value fields: first to get the manager, then
another to get the manager's manager
(C) Use Sum Related Instances
(D) Use Concatenate Text

**Correct Answer: (B)**

**Explanation:**
To traverse two levels of a relationship, you **chain** Lookup Related Value
fields. The first LRV retrieves the worker's manager (Worker -> Manager). The
second LRV takes that manager as input and retrieves their manager (Manager ->
Manager's Manager). This chaining approach works for any depth of relationship
traversal.

---

### Question 48

**What is "Extract Single Instance" used for?**

(A) Extracting a single numeric value from a text field
(B) Retrieving one specific instance from a multi-instance related business
object based on defined criteria
(C) Extracting the first character of a text field
(D) Removing duplicate instances from a report

**Correct Answer: (B)**

**Explanation:**
**Extract Single Instance** retrieves **one specific record** from a
multi-instance related business object based on criteria you define (e.g., the
most recent, the primary, or one matching a specific condition). For example,
extracting the primary home address from a worker's multiple addresses.

---

### Question 49

**A report needs to show the value of an employee's base pay as of a
specific historical date (e.g., January 1 of the current year), not the
current value. Which function should you use?**

(A) Lookup Related Value
(B) Lookup Value as of Date, configured with the Effective Date option
(C) Date Difference
(D) Arithmetic Calculation

**Correct Answer: (B)**

**Explanation:**
**Lookup Value as of Date** with the **Effective Date** option retrieves the
value of a field as it was on a specific date. This is essential for
point-in-time reporting, allowing you to see historical data rather than the
current value. The Effective Date option uses the business-effective date,
not the system-entry date.

---

### Question 50

**What is the difference between "Effective Date" and "Entry Date" options
in the "Lookup Value as of Date" function?**

(A) They are the same
(B) Effective Date returns the value as of the business-effective date
(when the change took effect); Entry Date returns the value as of the
system-entry date (when the change was entered into Workday)
(C) Effective Date is for future dates; Entry Date is for past dates
(D) Effective Date is for compensation; Entry Date is for job changes

**Correct Answer: (B)**

**Explanation:**
**Effective Date** reflects when the change **took business effect** (e.g., a
pay increase effective April 1). **Entry Date** reflects when the change **was
entered into the system** (e.g., the pay increase was entered on March 15 but
effective April 1). These two dates can differ significantly, and the choice
affects which version of the data is returned.

---
---

# SECTION G: AGGREGATION AND MULTI-INSTANCE

---

### Question 51

**A finance report needs to show the total expense amount across all expense
lines for each worker. Which function is correct?**

(A) Lookup Related Value
(B) Count Related Instances
(C) Sum Related Instances
(D) Extract Single Instance

**Correct Answer: (C)**

**Explanation:**
**Sum Related Instances** aggregates a numeric field across all instances of a
related multi-instance business object. In this case, it sums the "Amount"
field across all expense line instances for each worker, returning the total.

---

### Question 52

**What is the difference between "Sum Related Instances" and "Count Related
Instances"?**

(A) They are the same
(B) Sum aggregates a numeric field (totals values); Count returns the number
of instances (how many records exist)
(C) Sum works on text; Count works on numbers
(D) Sum counts unique values; Count counts all values

**Correct Answer: (B)**

**Explanation:**
**Sum Related Instances** adds up a numeric field across all related instances
(e.g., total dollar amount of all expenses). **Count Related Instances** returns
the **number of related instances** (e.g., how many expense lines exist). Sum
produces a total value; Count produces a count of records.

---

### Question 53

**You need to count the number of direct reports for each manager. The report
is based on the Worker business object. Which function do you use?**

(A) Arithmetic Calculation
(B) Evaluate Expression
(C) Count Related Instances (on the Direct Reports relationship)
(D) Lookup Related Value

**Correct Answer: (C)**

**Explanation:**
**Count Related Instances** on the Direct Reports multi-instance relationship
returns the number of workers who report to each manager. This function counts
the instances of the related object, which in this case is the set of direct
reports.

---

### Question 54

**Sum Related Instances can be configured with a filter to aggregate only
specific instances. True or False?**

(A) True -- you can apply a filter condition to aggregate only instances
that meet specific criteria
(B) False -- Sum Related Instances always aggregates all instances without
filtering

**Correct Answer: (A)**

**Explanation:**
**Sum Related Instances supports filtering** to aggregate only instances that
meet specified criteria. For example, you could sum only expense lines with a
status of "Approved" rather than all expense lines. The filter is configured
within the Calculated Field definition.

---

### Question 55

**A report needs the average salary of all workers in each supervisory
organisation. Which approach is correct?**

(A) Use Arithmetic Calculation: Total Salary / Number of Workers, where
Total Salary uses Sum Related Instances and Number of Workers uses
Count Related Instances
(B) Use a single Concatenate Text field
(C) Use Date Difference
(D) Use Extract Single Instance

**Correct Answer: (A)**

**Explanation:**
Average = Total / Count. Create a **Sum Related Instances** field to total the
salary across all workers in the org. Create a **Count Related Instances**
field to count the workers. Then create an **Arithmetic Calculation** that
divides the total by the count. This three-field approach produces the average.

---

### Question 56

**What does "Extract Multi-Instance" return?**

(A) A single value from one related instance
(B) Multiple values across all matching instances, typically as a
multi-valued result for reporting or further processing
(C) A count of instances
(D) An average of numeric values across instances

**Correct Answer: (B)**

**Explanation:**
**Extract Multi-Instance** returns multiple values from related instances,
producing a multi-valued result. This differs from Extract Single Instance
(which returns one value) and from Sum/Count (which return a single aggregated
value). Extract Multi-Instance is useful when you need to display all matching
values rather than a single aggregated result.

---
---

# SECTION H: ADVANCED SCENARIOS AND PERFORMANCE

---

### Question 57

**Scenario: A compensation report includes 15 Calculated Fields, and the
report takes over 60 seconds to run. A colleague suggests converting some
system-wide Calculated Fields to report-specific fields. Will this improve
performance?**

(A) Yes -- report-specific fields are always faster
(B) No -- there is no performance difference between system-wide and
report-specific Calculated Fields; the issue lies in the number and
complexity of the calculations themselves
(C) Yes -- but only if there are more than 20 fields
(D) No -- system-wide fields are always faster

**Correct Answer: (B)**

**Explanation:**
There is **no inherent performance difference** between system-wide and
report-specific Calculated Fields. Both are evaluated at runtime. Performance
is determined by the **number of fields, the complexity of each field's logic,
and whether they reference related objects requiring joins**. To improve
performance, reduce the number of fields, simplify logic, or use pre-joined
data sources.

---

### Question 58

**Scenario: You created an Evaluate Expression with 12 nested conditions
for a complex classification. The report runs slowly. What is the MOST
effective optimisation?**

(A) Convert the Evaluate Expression to 12 separate Arithmetic Calculations
(B) Reduce the number of conditions by grouping similar categories,
or move the classification to a Custom Report Data Source that pre-computes
the value
(C) Add more conditions to make the evaluation faster
(D) Convert to Concatenate Text

**Correct Answer: (B)**

**Explanation:**
Deeply nested Evaluate Expressions with many conditions can impact performance.
The best approach is to **simplify the logic** by grouping similar categories
or, for complex classifications, **move the computation to a Custom Report Data
Source (CRDS)** where the value is pre-computed and indexed for faster access.

---

### Question 59

**Scenario: An HR analyst requests a report showing each employee's tenure
category ("0-1 years", "2-5 years", "6-10 years", "10+ years"), their
manager's name, total compensation (base + bonus), and whether they are
benefits-eligible (must be full-time AND have 1+ year of tenure). How many
Calculated Fields do you need at minimum?**

(A) 2
(B) 4
(C) 5
(D) 7

**Correct Answer: (B)**

**Explanation:**
The minimum Calculated Fields required are:

1. **Date Difference** -- Tenure in years (Current Date - Hire Date)
2. **Evaluate Expression** -- Tenure category based on the Date Difference
   result (IF tenure <= 1 THEN "0-1 years", etc.)
3. **Arithmetic Calculation** -- Total Compensation (Base Pay + Bonus)
4. **Evaluate Expression** -- Benefits eligibility (IF Full-Time AND
   Tenure >= 1 THEN "Eligible" ELSE "Not Eligible")

The manager's name can be retrieved via Lookup Related Value or may be
available as a standard field on the data source, but in many configurations
it is a standard field. If it requires LRV, the answer would be 5.

---

### Question 60

**Scenario: A security administrator reports that a Calculated Field
displaying "Annual Bonus" data shows values for some users but returns
blank for others, even though all users have access to the report. The
Calculated Field uses Lookup Related Value to retrieve the bonus from
the Compensation business object. What is the MOST LIKELY cause, and
how should it be resolved?**

(A) The Calculated Field has a bug; rebuild it from scratch
(B) The users who see blanks do not have domain security access to the
Compensation domain; grant View access to the Compensation domain for
the appropriate security groups
(C) The report has a filter excluding certain users
(D) Lookup Related Value cannot retrieve compensation data

**Correct Answer: (B)**

**Explanation:**
Workday enforces **domain security at the field level**, even within Calculated
Fields. If a Calculated Field references data in a secured domain (e.g.,
Compensation), users without **View access** to that domain will see
**NULL/blank** values. The Calculated Field itself is not broken -- the security
configuration is working as designed. The resolution is to grant View access to
the Compensation domain via the appropriate domain security policy for the
affected security groups, then **activate** the pending security changes.

---
---

# QUICK-REFERENCE ANSWER KEY

| Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans | Q | Ans |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | B | 11 | B | 21 | B | 31 | B | 41 | B | 51 | C |
| 2 | B | 12 | C | 22 | B | 32 | B | 42 | B | 52 | B |
| 3 | C | 13 | B | 23 | B | 33 | B | 43 | B | 53 | C |
| 4 | B | 14 | B | 24 | B | 34 | B | 44 | C | 54 | A |
| 5 | B | 15 | B | 25 | B | 35 | B | 45 | B | 55 | A |
| 6 | B | 16 | B | 26 | B | 36 | B | 46 | C | 56 | B |
| 7 | B | 17 | B | 27 | A | 37 | B | 47 | B | 57 | B |
| 8 | B | 18 | B | 28 | C | 38 | B | 48 | B | 58 | B |
| 9 | C | 19 | C | 29 | B | 39 | B | 49 | B | 59 | B |
| 10 | B | 20 | B | 30 | B | 40 | B | 50 | B | 60 | B |

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

*End of Calculated Fields Examination -- 60 Questions*
