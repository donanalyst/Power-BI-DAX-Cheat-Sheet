# Aggregation Functions
Aggregation functions are used to summarize data. It will help the users to create a meaningful insights. 
These functions are typically applied in calculated measures, calculated columns, calculated tables, or visualizations. 

# SUM
Definition:
Calculates the total of all values in a column.

Syntax:
SUM(<column>)

Parameters:
(<column>): The column containing the numeric values to sum.

![image](https://github.com/user-attachments/assets/a2797498-e12b-4084-a380-36de4f89c05c)

# AVERAGE
Definition:
Calculates the arithmetic mean of the values in a column.

Syntax:
AVERAGE(<column>)

Parameters:
<column>: The column containing the numeric values to average.

![image](https://github.com/user-attachments/assets/ee27a8b9-c439-492b-aeb8-9e08a2f55981)


# COUNT 

Definition:
Counts the number of rows in a column that are not blank.

Syntax:
COUNT(<column>)

Parameters:
<column>: The column whose non-blank rows will be counted.

![image](https://github.com/user-attachments/assets/7ccc3bc4-8207-43d5-a3b8-8d4323f79825)

# COUNTROWS

Definition:
Counts the total number of rows in a table.

Syntax:
COUNTROWS(<table>)

Parameters:
<table>: The table to count rows from.

![image](https://github.com/user-attachments/assets/f3c4903e-27f0-42e0-9318-e49ed834d167)


# MAX
Definition:
Returns the largest numeric or date value in a column

Syntax:
MAX(<column>)

Parameters:
<column>: The column containing the numeric or date values.

![image](https://github.com/user-attachments/assets/a414b008-1f12-4e5f-9330-8bfebcb4b4f8)

# MIN

Definition:
Returns the smallest numeric or date value in a column.

Syntax:
MIN(<column>)

Parameters:
<column>: The column containing the numeric or date values.

![image](https://github.com/user-attachments/assets/5f2200c8-e8cf-4dc5-bdf9-17edbcface24)


# DISTINCTCOUNT

Definition:
Counts the number of unique values in a column.

Syntax:
DISTINCTCOUNT(<column>)

Parameters:
<column>: The column containing values to count distinct items.

![image](https://github.com/user-attachments/assets/783a0333-d519-426e-8e3e-5fee46cc872e)


# MEDIAM

Definition:
Calculates the median (middle value) of a set of numbers in a column.

Syntax:
MEDIAN(<column>)

Parameters:
<column>: The column containing numeric values.

![image](https://github.com/user-attachments/assets/24268385-3a60-444a-ada6-deb961784de5)


# VARIANCE
Definition:
Returns the variance of a column for the entire dataset.

Syntax:
VAR(<column>)

Parameters:
<column>: The column containing numeric values.

![image](https://github.com/user-attachments/assets/b09c007b-f39a-49cb-ab5c-2f7a5809a1f9)


# STDEV(Standard Deviation)

Definition:
Calculates the standard deviation of a column for the entire dataset.

Syntax:
STDEV(<column>)

Parameters:
<column>: The column containing numeric values.

![image](https://github.com/user-attachments/assets/deb7f270-ccbe-4226-950b-b337c02703aa)

# AGGREGATION WITH AN X 
There is an aggregation function in Power BI with an x at the end of the function, which has a different parameter but almost the same function as the one without it.
This function will create a new virtual column on the table that is being reference and will perform row by row context and summarize it at the end.

# SUMX
Definition:
Calculates the sum of an expression evaluated row by row in a table.

Syntax:
SUMX(table, expression)

Parameters:
table: The table to iterate over.

expression: The expression to evaluate for each row.

![image](https://github.com/user-attachments/assets/fcdb9bd4-42f9-4ff2-835e-4921208cbe66)


# AVERAGEX

Definition:
Calculates the average of an expression evaluated row by row in a table.

Syntax:
AVERAGEX(table, expression)

Parameters:
table: The table to iterate over.

expression: The expression to evaluate for each row.

![image](https://github.com/user-attachments/assets/8bf6261d-b44c-4d14-9ca0-d868cf7c5670)

# Other Aggregation Functions in Power BI:
MAXX: Returns the maximum value of an expression in a table.

MINX: Returns the minimum value of an expression in a table.

GEOMEAN: Calculates the geometric mean.

PERCENTILEX.INC: Calculates the inclusive percentile.

PERCENTILEX.EXC: Calculates the exclusive percentile.


# AGGREGATION WITH AN A
This type of function that will include not just numeric data data type.


# COUNTA

Definition: Counts the number of non-blank rows in a column, regardless of data type.

Syntax:
COUNTA(<column>)

Parameters:
<column>: The column containing values to count.


![image](https://github.com/user-attachments/assets/b6de4393-04a8-4e57-b88b-f291cd70bddb)

# AVERAGEA
Definition: Calculates the average of values in a column, including text and logical values.

-- Text is treated as 0.

-- Logical TRUE is treated as 1, and FALSE is treated as 0.

Syntax:

AVERAGEA(<column>)

Parameters:
<column>: The column containing values to average.

![image](https://github.com/user-attachments/assets/b334ecdb-6e41-4b24-9e45-105dc8e268b8)


# MAXA

Definition: Returns the largest value in a column, including logical and text values.

-- Text is evaluated in alphabetical order.

-- Logical TRUE is treated as 1, and FALSE as 0.

Syntax:
MAXA(<column>)

Parameters:
<column>: The column containing values to evaluate.

![image](https://github.com/user-attachments/assets/ea3bb340-b52d-493b-8839-c8a9d5952d28)

# MINA

Definition: Returns the smallest value in a column, including logical and text values.

-- Text is evaluated in alphabetical order.
-- Logical TRUE is treated as 1, and FALSE as 0.

Syntax:
MINA(<column>)

Parameters:
<column>: The column containing values to evaluate.

![image](https://github.com/user-attachments/assets/b606d09e-9194-494e-ae5b-62333edf2793)


# COUNTAX

Definition: Counts the number of non-blank results of an expression evaluated for each row in a table, even if the result is text or logical.

Syntax:
COUNTAX(table,expression)

Parameters:

<table>: The table to iterate over.
  
<expression>: The calculation to evaluate for each row.

![image](https://github.com/user-attachments/assets/4027f6c7-7b96-4cd8-b230-b47f3818729d)



























