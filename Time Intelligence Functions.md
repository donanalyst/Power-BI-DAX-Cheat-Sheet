# What is Time Intelligence Function in DAX Power BI?

Time Intelligence functions in DAX are designed to perform calculations over date and time periods.
These functions help you create measures and calculations that involve comparing, summing, or aggregating data 
across different time periods like months, quarters, and years.

# CLOSINGBALANCEMONTH

**Definition:** Calculates the value at the end of the last day of the month in the current context.

**Syntax:**

    CLOSINGBALANCEMONTH(<expression>, <dates>[, <filter>])

**Parameters:**

- expression: Numeric expression to evaluate.

- dates: A column containing date values.

- filter: (Optional) Additional filter context.

**Use Case:** Find the closing balance for monthly data.

**Example:**

    CLOSINGBALANCEMONTH(SUM(Sales[Amount]), Calendar[Date])

# CLOSINGBALANCEQUARTER

**Definition:** Calculates the value at the end of the last day of the quarter.

**Syntax:**

    CLOSINGBALANCEQUARTER(<expression>, <dates>[, <filter>])

**Example:**

    CLOSINGBALANCEQUARTER(SUM(Sales[Amount]), Calendar[Date])

# CLOSINGBALANCEYEAR

**Definition:** Calculates the value at the end of the last day of the year.

**Syntax:**

    CLOSINGBALANCEYEAR(<expression>, <dates>[, <filter>])

**Example:**

    CLOSINGBALANCEYEAR(SUM(Sales[Amount]), Calendar[Date])

# DATEADD

**Definition:** Shifts a set of dates by a specified interval.

**Syntax:**

    DATEADD(<dates>, <number_of_intervals>, <interval>)

**Parameters:**

- dates: A column containing dates.

- number_of_intervals: Positive or negative integer indicating the shift.

- interval: "DAY", "MONTH", "QUARTER", "YEAR".

**Use Case:** Compare data across time shifts.

**Example:**

    CALCULATE(SUM(Sales[Amount]), DATEADD(Calendar[Date], -1, "YEAR"))

# DATESBETWEEN

**Definition:** Returns a table with a set of dates between a specified start and end date.

**Syntax:**

    DATESBETWEEN(<dates>, <start_date>, <end_date>)

**Example:**

    CALCULATE(SUM(Sales[Amount]), DATESBETWEEN(Calendar[Date], DATE(2023, 1, 1), DATE(2023, 12, 31)))

# DATESINPERIOD

**Definition:** Returns a table with dates shifted by a specified interval relative to a given start date.

**Syntax:**

    DATESINPERIOD(<dates>, <start_date>, <number_of_intervals>, <interval>)

**Example:**

    CALCULATE(SUM(Sales[Amount]), DATESINPERIOD(Calendar[Date], TODAY(), -1, "YEAR"))

# DATESMTD


**Definition:** Returns a table with dates from the beginning of the current month to the current date.

**Syntax:**

    DATESMTD(<dates>)
    
**Example:**

    CALCULATE(SUM(Sales[Amount]), DATESMTD(Calendar[Date]))

# DATESQTD

**Definition:** Returns a table with dates from the beginning of the current quarter to the current date.

**Syntax:**

    DATESQTD(<dates>)

**Example:**

    CALCULATE(SUM(Sales[Amount]), DATESQTD(Calendar[Date]))

# DATESYTD

**Definition:** Returns a table with dates from the beginning of the year to the current date.

**Syntax:**

    DATESYTD(<dates>[, <year_end_date>])

**Example:**

    CALCULATE(SUM(Sales[Amount]), DATESYTD(Calendar[Date]))


# ENDOFMONTH

**Definition:** Returns the last date of the month in the current context.

**Syntax:**

    ENDOFMONTH(<dates>)

**Example:**

    CALCULATE(SUM(Sales[Amount]), ENDOFMONTH(Calendar[Date]))

# TOTALMTD

**Definition:** Calculates the month-to-date value for an expression.

**Syntax:**

    TOTALMTD(<expression>, <dates>[, <filter>])

**Example:**

    TOTALMTD(SUM(Sales[Amount]), Calendar[Date])

# SAMEPERIODLASTYEAR

**Definition:** Returns a set of dates from the same period in the previous year.

**Syntax:**

    SAMEPERIODLASTYEAR(<dates>)

**Example:**

    CALCULATE(SUM(Sales[Amount]), SAMEPERIODLASTYEAR(Calendar[Date]))


# PREVIOUSYEAR

**Definition:** Returns the dates for the entire previous year.

**Syntax:**

    PREVIOUSYEAR(<dates>)

**Example:**

    CALCULATE(SUM(Sales[Amount]), PREVIOUSYEAR(Calendar[Date]))

# Key Uses of Time Intelligence Functions 

**1. Trend Analysis:** Compare metrics over time, such as year-over-year growth.

**2. Cummulative Totals:** Calculate running totals for month-to-date, quarter-to-date, or year-to-date.

**3. Forecasting:** Use historical data to predict future performance.

**4. Dynamic Aggregation:** Create measure that adapt based on the user's time-based selections.











