# Input Function, Python Type Casting and Calculations

## Input Functions

Programs often require user input from the keyboard

input function captures keyboard data and returns it as a string, typically used in an assignment statement as follows:

   `variable = input(prompt)`

   `name = input('What is your name')`

Example:

`first_name = input('What is your first name')`

`last_name = input('What is your last name')`

`print("Hello", first_name, last_name)`



## Python Type Casting

Type casting means changing from one data type to another.

Python built-in conversion functions:

`int()`  : Converts a string to an integer (Whole number)

`float()`  : Converts a string to a floating-point number (Decimal number)

`str()`  : Converts any value back to a string (Text)



How to type cast?

`a = "10"`  ("a" has a string class)

`b = int(a)` (converts "a" string class to a integer)



btw

if a = 10, "a" is an integer.

if a = 10.0, "a" is a float.

if a = "10", "a" is a string



The `int()` and `float()` only works if the argument that is being converted contains a numeric value. If not a `ValueError` type of error will occur and the program will stop.

## Calculations

Basic Arithmetic Operators for Python

![image.png](Programming%20notes.assets/image%20(8).png)

Python's operator precedence follows the BODMAS rule

![image.png](Programming%20notes.assets/image%20(9).png)



Basic incremental and decremental:

`x = x + 1` is the same as `x += 1`, increase x by 1

`x -= (y +7)` is the same as `x = x- (y + 7)`, reduce x value by (y +7)



Python also has built-in support for more complex math operations and functions such as trigonometric functions, logarithms and exponentiation.

![image.png](Programming%20notes.assets/image%20(10).png)

