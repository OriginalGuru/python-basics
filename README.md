# Python Fundamentals Assignment

Welcome to your first Python assignment! In this task, you will explore the foundational elements of Python programming, focusing on native Python features. This assignment is designed to be completed using Jupyter Notebooks, which will allow you to run and test your code interactively.

## Objectives

By the end of this assignment, you will:

1. Understand and use basic arithmetic operations in Python.
2. Assign and manipulate variables.
3. Utilize basic logical operators.
4. Seek help in Python using built-in functions.
5. Manage and interpret error messages.
6. Use special characters (`;`, `\`, `{}`, `()`, and `[]`) effectively in Python code.

## Getting Started

Clone this repository to your local machine and open the provided Jupyter Notebook (`python_fundamentals.ipynb`) in your preferred environment (e.g., VSCode, Jupyter Lab, or Jupyter Notebook).

## 1. Basic Arithmetic Operations in Python

Python provides several native operations that you will use frequently. In this section, you will practice the following operations:

- Addition (`+`)
- Subtraction (`-`)
- Multiplication (`*`)
- Division (`/`)
- Exponentiation (`**`)
- Modulus (`%`)
- Floor Division (`//`)

### Task:

1. Create variables `a` and `b` with values of your choice.
2. Perform each of the above operations using `a` and `b`.
3. Print the results.

```python
a = 10
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

## 3. Logical Operators

Logical operators are essential in decision-making processes.
Task:

    Explore the use of and, or, and not.
    Create expressions that evaluate to True or False using these operators.

```python
is_greater = x > y and y < z
is_equal = x == y or y == z
negation = not is_greater
```

## 4. Getting Help in Python

Python provides built-in functions to get help and explore the capabilities of objects.
Task:

    Use the dir() function to list the attributes and methods of an object.
    Use the ? and ?? operators to access the docstring and source code of functions.

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

# TypeError
result = "string" + 5

# SyntaxError
if x > y
    print("x is greater")
```

## 6. Using Special Characters: {}, (), and []

Python uses different brackets for various purposes:

    {}: Used for dictionaries and string formatting.
    (): Used for tuples, function calls, and expressions.
    []: Used for lists, indexing, and slicing.

Task:

    Create a dictionary, tuple, and list.
    Access elements and perform operations on them.

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

