# Logical Functions in DAX 

Logical functions in DAX are used to evaluate expressions and return Boolean Values (TRUE or FALSE) or control the flow of logic
in your calculations. They are commonly used for conditions, error handling, and decision-making.

# AND

**Definition:** Returns TRUE if both arguments are TRUE.

**Syntax:**

    AND(<logical1>, <logical2>)
    
**Parameters:**

- logical1: First logical expression.
  
- logical2: Second logical expression.
  
**Use Case:** Combine two conditions.

**Example:**

    AND(Sales[Amount] > 100, Sales[Quantity] > 2)

# BITAND

**Definition:** Performs a bitwise AND operation.

**Syntax:**

    BITAND(<number1>, <number2>)
    
**Parameters:**

- number1: First number.

- number2: Second number.

**Use Case:** Bitwise operations for integer comparison.

**Example:**

    BITAND(6, 3) // Result: 2

# BITSHIFT

**Definition:** Shifts the bits of a number to the left.

**Syntax:**

    BITLSHIFT(<number>, <shift_amount>)
    
**Parameters:**

- number: The number to shift.

- shift_amount: The number of positions to shift.

**Use Case:** Perform left bitwise shifts.

**Example:**

    BITLSHIFT(3, 2) // Result: 12

# BITOR

**Definition:** Performs a bitwise OR operation.

**Syntax:**

    BITOR(<number1>, <number2>)
**Parameters:**

- number1: First number.

- number2: Second number.

**Use Case:** Bitwise operations for integer comparison.

**Example:**

    BITOR(6, 3) // Result: 7

# BITRSHIFT

**Definition:** Shifts the bits of a number to the right.

**Syntax:**

    BITRSHIFT(<number>, <shift_amount>)
    
**Parameters:**

- number: The number to shift.

- shift_amount: The number of positions to shift.

**Use Case:** Perform right bitwise shifts.

**Example:**

    BITRSHIFT(8, 2) // Result: 2

# BITXOR

**Definition:** Performs a bitwise XOR operation.

**Syntax:**

    BITXOR(<number1>, <number2>)
    
**Parameters:**

- number1: First number.

- number2: Second number.

**Use Case:** Bitwise exclusive OR operations.

**Example:**

    BITXOR(6, 3) // Result: 5

# COALESCE

**Definition:** Returns the first non-blank value from the arguments.

**Syntax:**

    COALESCE(<value1>, <value2>, ...)
    
**Parameters:**

- value: List of values to evaluate.
  
**Use Case:** Handle missing or blank values.

**Example:**

    COALESCE(Sales[Amount], 0)

# FALSE

**Definition:** Returns the Boolean value FALSE.

**Syntax:**

    FALSE()
    
**Use Case:** Explicitly use FALSE in logical expressions.

Example:

    IF(FALSE(), "Yes", "No")

# IF 

**Definition:** Evaluates a condition and returns one value if TRUE and another if FALSE.

**Syntax:**

    IF(<logical_test>, <value_if_true>, <value_if_false>)
    
**Parameters:**

- logical_test: Condition to evaluate.

- value_if_true: Value if condition is TRUE.

- value_if_false: Value if condition is FALSE.

**Use Case:** Perform conditional logic.

**Example:**

    IF(Sales[Amount] > 100, "High", "Low")

# IFERROR

**Definition:** Returns a value if the expression results in an error; otherwise, returns the expression result.

**Syntax:**

    IFERROR(<value>, <value_if_error>)

**Parameters:**

- value: Expression to evaluate.

- value_if_error: Value to return if an error occurs.

**Use Case:** Handle errors gracefully.

**Example:**

    IFERROR(SUM(Sales[Amount]), 0)


# NOT

**Definition:** Reverses a logical value.

**Syntax:**

    NOT(<logical>)
    
**Parameters:**

- logical: A logical expression.

**Use Case:** Negate Boolean values.

**Example:**

    NOT(Sales[Amount] > 100)

# OR 

**Definition:** Returns TRUE if any argument is TRUE.

**Syntax:**

    OR(<logical1>, <logical2>)

**Parameters:**

- logical1: First logical expression.

- logical2: Second logical expression.

**Use Case:** Combine multiple conditions.

**Example:**

    OR(Sales[Amount] > 100, Sales[Quantity] > 2)

# SWITCH

**Definition:** Evaluates an expression against a list of values and returns the corresponding result.

**Syntax:**

    SWITCH(<expression>, <value>, <result>[, <value>, <result>, ...][, <else_result>])

**Parameters:**

- expression: Expression to evaluate.

- value: Value to compare against.

- result: Result to return.

- else_result: Default result if no match is found.

**Use Case:** Simplify complex conditional logic.

**Example:**

    SWITCH(Sales[Region], "North", 1, "South", 2, "Other")

# TRUE 

**Definition:** Returns the Boolean value TRUE.

**Syntax:**

    TRUE()

**Use Case:** Explicitly use TRUE in logical expressions.

**Example:**

    IF(TRUE(), "Yes", "No")










