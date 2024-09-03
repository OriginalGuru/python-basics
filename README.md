# Python Basics

In this task, we'll explore some of the foundational elements of Python programming, focusing on native Python features. This assignment is designed to be completed using Jupyter Notebooks, which will allow you to run and test your code interactively.

## Objectives

By the end of this assignment, you will:

1. Understand and use basic arithmetic operations in Python.
2. Assign and manipulate variables.
3. Use basic comparisson and logical operators.
4. Seek help in Python using built-in functions.
5. Manage and interpret some common error messages.
6. Use several special characters (`;`, `\`, `{}`, `()`, and `[]`) in basic Python code.

## Getting Started

Clone this repository to your local machine and open the provided Jupyter Notebook (`python_fundamentals.ipynb`) in Jupyter Notebook.

## 1. Basic Arithmetic Operations in Python

Python provides several native operations that you will use frequently. In this section, you will practice the following operations:

- Addition (`+`)
- Subtraction (`-`)
- Multiplication (`*`)
- Division (`/`)
- Exponentiation (`**`)

There are also a few less common operations that you might see:

- Modulus (`%`)
- Floor Division (`//`)

### Task:

1. Create variables `a` and `b` with values of your choice.
2. Perform each of the above operations using `a` and `b`.
3. Print the results.

```python
a = 10.2
b = 3

# Example:
addition = a + b
print(f"Addition: {addition}")
# Repeat for other operations
```

## 2. Variable Assignment and Manipulation

Variables in Python are used to store data that can be reused and manipulated.
Task:

    Assign values to variables x, y, and z.
    Reassign and manipulate these variables.
    Explore the use of the semicolon (;) to write multiple statements on a single line.
    Use the backslash (\) to continue long lines of code.

```python
x = 5
y = 10
z = x + y

# Using semicolon
a = 1; b = 2; c = a + b

# Using backslash
long_sum = x + y + z + a + b + c + \
           100 + 200 + 300
```

## 3. Comparison and Logical Operators
Comparison Operators

Comparison operators are used to compare two values:

    <: Less than
    >: Greater than
    ==: Equal to
    !=: Not equal to
    <=: Less than or equal to
    >=: Greater than or equal to

Logical Operators

Logical operators combine multiple comparison expressions:

    and: Returns True if both expressions are true.
    or: Returns True if at least one expression is true.
    not: Inverts the boolean value of an expression.

Task:

    Use comparison operators to evaluate conditions between two variables.
    Combine these conditions using logical operators to create more complex expressions.

```python
x = 7
y = 10

# Comparison operators
is_x_less_than_y = x < y  # True
is_y_equal_to_10 = y == 10  # True

# Logical operators
is_x_between_5_and_15 = (x > 5) and (x < 15)  # True
is_y_10_or_greater = y >= 10 or y < 5  # True
is_not_equal_to_7 = not (x == 7)  # False

print(is_x_less_than_y)
print(is_x_between_5_and_15)
```

## 4. Getting Help in Python

Python provides built-in functions to get help and explore the capabilities of objects.
Task:

    Use the dir() function to list the attributes and methods of an object.
    In Jupyter Notebook, use the ? and ?? operators to access the docstring and source code of functions.

```python
dir(str)
help(str.lower)
str.lower?
str.lower??
```

Additionally, refer to the [Python documentation](https://docs.python.org/3/) for more detailed syntax and usage.

## 5. Managing Error Messages

Errors are a natural part of programming. Understanding them is crucial for debugging.
Task:

    Intentionally create common errors (e.g., NameError, TypeError, SyntaxError).
    Examine the error messages, noting the order of information presented.
    Identify the type of error and common causes.

```python
# NameError
print(undefined_variable)
```

```python
# TypeError
result = "string" + 5
```

```python
# SyntaxError
if x > y
    print("x is greater")
```

## 6. Lists, tuples, and disctionaries: [], (), and {}

Python uses different brackets for various purposes:

    []: Used for lists, indexing, and slicing.
    (): Used for tuples, function calls, and expressions.
    {}: Used for dictionaries and string formatting.

Task:

    Create a dictionary, tuple, and list.
    Access elements and perform operations on them.

Note:
    Python starts indexing at 0, so the first element of a list 'my_list' would be mylist(0)

```python
# Dictionary
my_dict = {"name": "Python", "version": 3.9}

# Tuple
my_tuple = (1, 2, 3)

# List
my_list = [1, 2, 3, 4, 5]

# Accessing elements
print(my_dict["name"])
print(my_tuple[0])
print(my_list[2:4])
```

## Assignment: Creating a Conversion Dictionary

Objective:
The goal of this assignment is to create a simple Python dictionary that stores conversion factors between different descriptors of waves  and a Boolean flag indicating whether the relationship between the units is an inverse relationship.

Part 0: Basic equations being used

The relationship between a waves characteristic length (or inverse length) and its frequency (or period) is called a dispersion relation. This can also be extended to energy quantities.

For light in vacuum, some common ways of expressing this dispersion relation are:

    $f = c/\lambda$ : the linear frequency is related to the wavelength, $\lambda$, by the speed of light, $c$. 
    
    $\omega = c k$ : the angular frequency is related to the angular wavevector/wavenumber, $k$, by the speed of light. 
    
    $\lambda/T = c$ : here $T$ is the period.  
    
    $E = h f = \hbar \omega = \hbar c k $ : here $h$ is Planck's constant and $\hbar$ is the reduced Planck's constant.  
    
    $k = 2 \pi \nu$ : $\nu$ is the linear wavenumber.  

Check the units to help you remember these dispersion relations.

Part 1: Understanding the Units

1. Units to Consider:

    THz: terahertz (Frequency)
    ps: picoseconds (Period)
    cm⁻¹: inverse centimeters (Wavenumber)
    nm: nanometers (Wavelength)
    meV: millielectronvolts (energy) 

Part 2: Conversion Relationships and Factors

2. Conversion Relationships: Use the dispersion relations to find how the various units are related

    Linear Frequency to Period (THz to ps): Inverse relationship: $T = 1/f$
    Angular Frequency to Wavenumber (THz to cm⁻¹): Direct relationship: $k = \omega/c$
    Linear Frequency to Wavelength (THz to nm): Inverse relationship: $\lambda = c/f$

Part 3: Creating the Dictionary

3. Dictionary Construction:

Your task is to create a Python dictionary that includes the following, for the units described above:

    A tuple as the key, representing the units to convert between (e.g., ("THz", "ps")).
    A value that is another tuple containing:
        The conversion factor (a number).
        A Boolean True or False indicating whether the conversion is inverse.


```python
# Conversion factors and inverse relationship flag
conversion_factors = {
    ("THz", "ps"): (1, True),                # Linear Frequency to Period (inverse; T=1/f)
    ("ps", "THz"): (1, True),                # Period to Linear Frequency (inverse; f=1/T)
    ("THz", "cm-1"): (33.356, False)         # Linear Frequency to Linear Wavenumber (k = f/c)
}

# Example of how to access the dictionary
# Let's say we want to convert from THz to ps
conversion_key = ("THz", "ps")

if conversion_key in conversion_factors:
    factor, is_inverse = conversion_factors[conversion_key]
    print(f"Conversion factor: {factor}")
    print(f"Is inverse relationship: {is_inverse}")
else:
    print("Conversion not supported.")
```

