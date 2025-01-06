# What are Filter Functions in DAX?

Filter Functions in DAX are a category of functions designed to work with filter contexts in your data
model. These functions allow you to modify, query, or evaluate rows based on specific conditions. They play
a critical role in defining dynamic calculations, aggregations, and filtering logic in Power BI, Excel Power Pivot, 
and Analysis Services.

# When to Use Filter Functions?

**Custom Filters:** Apply dynamic filtering based on user selections.

**Totals and Subtotals:** Create totals that respect or ignor specific filters.

**Conditional Calculations:** Perform calculations only under specific conditions.

**Row-Level Calculations:** Define row-wise filters or aggregations.


# FILTER

**Definition:** Returns a table with rows filtered based on a condition.

**Syntax:**

     FILTER(<table>, <condition>)
     
**Parameters:**

- table: The table to filter.

- condition: A logical expression.

**Use Case:** Apply filters dynamically in calculations.

**Example:**

    FILTER(Sales, Sales[Quantity] > 10)

# ALL

**Definition:** Removes all filters applied to a table or column.

**Syntax:**

    ALL([<table_or_column>])
    
**Parameters:**

- table_or_column: The table or column to clear filters from.

**Use Case:** Use in calculations that require ignoring filters, like totals.

**Example:**

    CALCULATE(SUM(Sales[Amount]), ALL(Sales[Region]))

# ALLCROSSFILTERED

**Definition:** Clears filters applied due to cross-filtering.

**Syntax:**

    ALLCROSSFILTERED(<table>)
    
**Parameters:**

- table: The table to clear cross-filters from.

**Use Case:** Ignoring cross-filter effects in calculations.

**Example:**

    CALCULATE(SUM(Sales[Amount]), ALLCROSSFILTERED(Sales))

# ALLEXCEPT

**Definition:** Removes filters from all columns except specified ones.

**Syntax:**

    ALLEXCEPT(<table>, <column>[, <column>])
    
**Parameters:**

- table: The table to clear filters from.
- column: Columns to retain filters.
  
**Use Case:** Retain specific filters while clearing others.

**Example:**

    CALCULATE(SUM(Sales[Amount]), ALLEXCEPT(Sales, Sales[Region])

# ALLNOBLANKROW

**Definition:** Removes all filters except for blank rows.

**Syntax:**

    ALLNOBLANKROW(<table_or_column>)
    
**Parameters:**

- table_or_column: The table or column to clear filters from.
  
**Use Case:** Ignore all rows except blank ones.

**Example:**

    CALCULATE(SUM(Sales[Amount]), ALLNOBLANKROW(Sales[Region]))

# ALLSELECTED

**Definition:** Returns all rows visible in the current query context.

**Syntax:**

    ALLSELECTED([<table_or_column>])
    
**Parameters:**
- table_or_column: The table or column to reference.

**Use Case:** Calculate totals respecting slicers.

**Example:**
  
    CALCULATE(SUM(Sales[Amount]), ALLSELECTED(Sales))

# CALCULATE

**Definition:** Modifies the filter context of an expression.

**Syntax:**

    CALCULATE(<expression>, <filter1>[, <filter2>, ...])
    
**Parameters:**

- expression: The calculation to perform.
- filter: Conditions to apply.

**Use Case:** Change filters dynamically.

**Example:**

    CALCULATE(SUM(Sales[Amount]), Sales[Region] = "North")

# CALCULATETABLE

**Definition:** Similar to CALCULATE, but returns a table instead of a scalar value.

**Syntax:**

    CALCULATETABLE(<table>, <filter1>[, <filter2>, ...])
    
**Parameters:** Same as CALCULATE.

**Use Case:** Create a filtered table.

**Example:**

    CALCULATETABLE(Sales, Sales[Region] = "North")

# EARLIER

**Definition:** Refers to a row context from an outer loop.

**Syntax:**

    EARLIER(<column>, <level>)
    
**Parameters:**
- column: Column to reference.
- level: Outer row context level.

**Use Case:** Calculate row-wise aggregates with nested contexts.

**Example:**

    FILTER(Sales, Sales[Amount] > EARLIER(Sales[Amount]))

# EARLIEST

**Definition:** Refers to the outermost row context.

**Syntax:**

    EARLIEST(<column>)
    
**Parameters:**
- column: Column to reference.

Use Case: Compare against the first row context.

**Example:**

    FILTER(Sales, Sales[Amount] > EARLIEST(Sales[Amount]))

# FIRSTNONBLANK

**Definition:** Returns the first non-blank value in a column.

**Syntax:**

    FIRSTNONBLANK(<column>, <expression>)
    
**Parameters:**

- column: Column to evaluate.
- expression: Expression to calculate.

**Use Case:** Return the first valid value.

**Example:**

    FIRSTNONBLANK(Sales[Product], Sales[Amount])

# FIRSTNONBLANKVALUE

**Definition:** Similar to FIRSTNONBLANK but returns a value calculated from the first row.

**Syntax:**

    FIRSTNONBLANKVALUE(<column>, <expression>)

**Parameters:** Same as FIRSTNONBLANK.

**Use Case:** Combine first-row filtering with calculations.

# LOOKUPVALUE

**Definition:** Retrieves a value from a column in another table.

**Syntax:**

    LOOKUPVALUE(<result_column>, <search_column1>, <search_value1>[, <search_column2>, <search_value2>])
    
**Parameters:**

- result_column: Column to return the value from.
- search_column: Column to search in.
- search_value: Value to match.

**Use Case:** Perform exact matches.

**Example:**

    LOOKUPVALUE(Sales[Amount], Sales[Product], "Laptop")

# WINDOW

**Definition:** Performs calculations over a window of rows.

**Syntax:**


    WINDOW(<table>, <expression>, <window_specification>)
    
**Parameters:**

- table: Table to operate on.
- expression: Calculation to apply.
- window_specification: Defines the window size and range.

**Use Case:** Rolling calculations (e.g., running totals).



