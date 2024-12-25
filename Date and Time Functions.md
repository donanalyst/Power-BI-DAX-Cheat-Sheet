# What are Date and Time Functions?
Date and time functions in Power BI allow you to work with dates and times, such as extracting parts of a date
(year, month, day), performing calculations(adding days, finding differences), and formatting dates.

These functions are particularly useful in analyzing time-based data, creating dynamic reports, and handling series data.


# DATE 

**Definition:** Returns the specified date (datetime).

**Syntax:**
DATE(year, month, day)

**Parameters:**

**year:** (Required) A number representing the year.

**month:** (Required) A number representing the month.

**day:** (Required) A number representing the day.

**Use:** Used to create a date when you have year, month, and day components separately.

**Example:**

     DATE(2023, 12, 25)

**Result:** 12/25/2023

# TODAY

**Definition:** Returns the current date.

**Syntax:**

    TODAY()

**Parameters:**
   None.

Use: To get the current date without the time component.

**Example:**

    TODAY()
    
**Result:** 12/25/2024 (example based on the current date).


# NOW 

**Definition:** Returns the current date and time.

**Syntax:**

    NOW()

**Parameters:**
  None.

**Use:** To get the current date and time.

**Example:**

    NOW()
  
**Result:** 

12/25/2024 8:00:00 AM (example based on current date and time).

# YEAR

**Definition:** Returns the year from a given date.

**Syntax:**

    YEAR(date)

**Parameters:**

**date:** (Required) A datetime value.

**Use:** Extracts the year part of a date.

**Example:**

    YEAR(DATE(2023, 12, 25))

**Result:** 2023

# MONTH

**Definition:** Returns the month from a given date as a number (1 = January, 12 = December).

**Syntax:**

    MONTH(date)

**Parameters:**

**date:** (Required) A datetime value.

**Use:** Extracts the month part of a date.

**Example:**

    MONTH(DATE(2023, 12, 25))
  
**Result:** 12

# DAY

**Definition:** Returns the day of the month from a given date.

**Syntax:**

    DAY(date)

**Parameters:**

**date:** (Required) A datetime value.

**Use:** Extracts the day part of a date.

**Example:**

    DAY(DATE(2023, 12, 25))

**Result:** 25

# TIME

**Definition:** Returns a time (datetime) value based on the hour, minute, and second.

**Syntax:**

    TIME(hour, minute, second)

**Parameters:**

**hour:** (Required) The hour component (0-23).

**minute:** (Required) The minute component (0-59).

**second:** (Required) The second component (0-59).

**Use:** Creates a time value.

**Example:**

    TIME(15, 30, 0)
  
**Result:** 3:30:00 PM

# HOUR

**Definition:** Returns the hour component from a time value.

**Syntax:**

    HOUR(time)

**Parameters:**

**time:** (Required) A datetime or time value.

**Use:** Extracts the hour part of a time.

**Example:**

    HOUR(TIME(15, 30, 0))
  
**Result:** 15

# MINUTE

**Definition:** Returns the minute component from a time value.

**Syntax:**

    MINUTE(time)

**Parameters:**

**time:** (Required) A datetime or time value.

**Use:** Extracts the minute part of a time.

**Example:**

    MINUTE(TIME(15, 30, 0))
  
**Result:** 30

# SECOND

**Definition:** Returns the second component from a time value.

**Syntax:**

    SECOND(time)

**Parameters:**

**time:** (Required) A datetime or time value.

**Use:** Extracts the second part of a time.

**Example:**

    SECOND(TIME(15, 30, 0))
  
**Result:** 0

# WEEKDAY

**Definition:** Returns the day of the week as a number.

**Syntax:**

    WEEKDAY(date, [return_type])

**Parameters:**

**date:** (Required) A datetime value.

**return_type:** (Optional) A number that determines the type of return value:

  1 (Default): Sunday = 1 to Saturday = 7.
  
  2: Monday = 1 to Sunday = 7.
  
  3: Monday = 0 to Sunday = 6.
  
**Use:** To identify the day of the week.

**Example:**

    WEEKDAY(DATE(2023, 12, 25), 1)
  
**Result:** 2 (Monday).

# WEEKNUM

**Definition:** Returns the week number of the year.

**Syntax:**

    WEEKNUM(date, [return_type])

**Parameters:**

**date:** (Required) A datetime value.

**return_type:** (Optional) Determines the week start:

   1 (Default): Week starts on Sunday.
   
   2: Week starts on Monday.
   
**Use:** To determine which week of the year a date falls into.

**Example:**

    WEEKNUM(DATE(2023, 12, 25), 1)
  
**Result:** 52

# EOMONTH

**Definition:** Returns the last day of the month for a given date.

**Syntax:**

    EOMONTH(start_date, months)

**Parameters:**

**start_date:** (Required) A datetime value.

**months:** (Required) The number of months to add (can be negative).

**Use:** To calculate the end of the month for a given date.

**Example:**

    EOMONTH(DATE(2023, 12, 25), 0)
  
**Result:** 12/31/2023

# DATEDIF

**Definition:** Returns the difference between two dates.

**Syntax:**

    DATEDIFF(start_date, end_date, interval)

**Parameters:**

**start_date:** (Required) A datetime value.

**end_date:** (Required) A datetime value.

**interval:** (Required) The unit of difference (DAY, MONTH, YEAR, etc.).

**Use:** To calculate date differences.

**Example:**

    DATEDIFF(DATE(2023, 12, 25), DATE(2024, 12, 25), YEAR)
  
**Result:** 1

# FORMAT

**Definition:** Returns a date formatted as text.

**Syntax:**

    FORMAT(value, format_string)

**Parameters:**

**value:** (Required) A datetime value.

**format_string:** (Required) A string specifying the format.

**Use:** To format dates and times as strings.

**Example:**

    FORMAT(DATE(2023, 12, 25), "YYYY/MM/DD")
  
**Result:** 2023/12/25


# CALENDAR

**Definition:**

Creates a single-column table of dates from a specified start date to an end date.


     CALENDAR(<start_date>, <end_date>)

**Parameters:**

<start_date>: The starting date of the calendar.

<end_date>: The ending date of the calendar.

**Uses:**

To generate a continuous range of dates for time intelligence calculations.

**Example:**

     CALENDAR(DATE(2024, 1, 1), DATE(2024, 12, 31))

**Result:** Generates a table of dates for the year 2024.

# CALENDARAUTO

**Definition:**
Automatically generates a single-column table of dates, spanning all date columns in the model.

**Syntax:**

    CALENDARAUTO([<fiscal_year_end_month>])

**Parameters:**

   [<fiscal_year_end_month>] (optional): Specifies the fiscal year-end month (default is December).
   
**Uses:**

Quickly generate a date table without manually specifying start and end dates.

**Example:**

    CALENDARAUTO(6)
    
**Result:** Generates dates considering the fiscal year ends in June.

# DATEVALUE

**Definition:** Converts a date in text format to a date/time data type.

**Syntax:**

    DATEVALUE(<date_text>)

**Parameters:**

    <date_text>: A text string representing a date.

**Uses:** To convert text-based dates into a date data type for calculations.

**Example:**

    DATEVALUE("2024-12-25")
    
**Result:** Returns 25th December 2024 as a date.


# EDATE

**Definition:** Returns the date that is the specified number of months before or after a given date.

**Syntax:**

    EDATE(<start_date>, <months>)
    
**Parameters:**

    <start_date>: The base date.
    
    <months>: The number of months to add (positive) or subtract (negative).
    
**Uses:** To calculate future or past dates based on a monthly interval.

**Example:**

    EDATE(DATE(2024, 12, 25), -3)
    
**Result:** Returns 25th September 2024.

# NETWORKDAYS

**Definition:**

Calculates the number of whole working days between two dates, excluding weekends and optionally specified holidays.

**Syntax:**

    NETWORKDAYS(<start_date>, <end_date>, [<holidays>])
    
**Parameters:**

    <start_date>: The start date.
    
    <end_date>: The end date.
    
    [<holidays>] (optional): A list of holiday dates to exclude.
    
**Uses:** To calculate the total working days between two dates.

**Example:**

    NETWORKDAYS(DATE(2024, 12, 1), DATE(2024, 12, 31), {DATE(2024, 12, 25)})
    
**Result:** Excludes weekends and 25th December 2024.

# QUARTER

**Definition:** Returns the quarter of the year for a date as a number (1 to 4).

**Syntax:**

    QUARTER(<date>)
    
**Parameters:**

  <date>: A date.
  
**Uses:** To identify or group data by quarters.

**Example:**

    QUARTER(DATE(2024, 12, 25))
    
**Result:** Returns 4 (fourth quarter).

# TIMEVALUE

**Definition:** Converts a time in text format to a time data type.

**Syntax:**

    TIMEVALUE(<time_text>)
    
**Parameters:**

    <time_text>: A text string representing a time.
    
**Uses:** To convert text-based times into a time data type.

**Example:**

    TIMEVALUE("14:30:00")
    
**Result:** Returns 2:30 PM.

# UTCNOW

**Definition:** Returns the current date and time in UTC.

**Syntax:**

    UTCNOW()

**Uses:** To capture the current UTC date and time for time zone-independent reporting.

**Example:**

    UTCNOW()
    
**Result:** Returns the current date and time in UTC.

# UTCTODAY

**Definition:** Returns the current date in UTC, with the time portion set to 12:00 AM.

**Syntax:**

    UTCTODAY()
    
**Uses:** To capture the current UTC date without the time.

**Example:**

    UTCTODAY()
    
**Result:** Returns today’s date in UTC.

# YEARFRAC

**Definition:**

Calculates the fraction of the year between two dates.

**Syntax:**

    YEARFRAC(<start_date>, <end_date>, [<basis>])
    
**Parameters:**

    <start_date>: The start date.
    
    <end_date>: The end date.
    
    [<basis>] (optional): The day-count basis (default is 0 for US 30/360).
    
**Uses:** To compute proportions of years for financial calculations like interest rates.

**Example:**

    YEARFRAC(DATE(2024, 1, 1), DATE(2024, 6, 30))
    
**Result:** Returns 0.5 (half a year).

