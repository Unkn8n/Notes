#### Topic 2.1

#### Strings and String Literals

In Python, strings must be enclosed in quotation marks. You can enclose a string literal in single or double quotation marks.

`print("Hello world")`

`print('Hello world')`

These are used to store words, sentences or even numbers as text.

You may click the "tab" key for quick completion of the code.

(Not always correct so do double check)



To include a single quote in a string literal, enclose the string in double quotes.

Conversely, use single quotes if the string contains double quotes.

`print('He said "cuh"')`

`print("I'm dead cuh")`

You can also add a "\" to tell python that the apostrophe is part of the text

`print(' I\'m crine ')`

If you do it wrongly, there will be SyntexError.



#### Comments and Variables

#### Comments

"#" is a comment

Python will not execute lines that have "#" at the start of their line as they will not be part of the code.

We use comments to help us understand the code that we have written.

Example:

![image.png](Programming%20notes.assets/image%20(7).png)

This is so collaborators understand what is going on in the code. It is a good practice to comment your codes incase you get lost on your own.

#### Variables

A variable is a name that represents a storage location in the computer's memory.

Variables consists of 3 different elements, a symbolic name, a assignment operator "=" and the value we want to store.

`age = 40`  (age being the variable and "40" being the value)

It is good practice to choose meaningful names that reflect the variable's content for easier identification when someone revisits your codes.

Things to note:

1. Variables can start with a letter or an underscore
2. It can consist of letters, underscore and numbers but no special characters
3. It is case sensitive
4. It cannot begin with a number
5. Cannot have spaces, it can be replaced with an underscore
6. Variables can't use Python's reserved keywords as variable names
   - To check, key in

      `import keyword`

      `print(keyword.kwlist)`

You can reassign existing variables to a new value, similar to how you would create a new variable.

`x = 2`         ←Assignment statement

`x = x + 2` ←Assignment with expression

`print(x)`   ←Print statement



#### Input Function, Python Type Casting and Calculations

**Input Functions**

Programs often require user input from the keyboard

input function captures keyboard data and returns it as a string, typically used in an assignment statement as follows:

   `variable = input(prompt)`

   `name = input('What is your name')`

Example:

`first_name = input('What is your first name')`

`last_name = input('What is your last name')`

`print("Hello", first_name, last_name)`



#### Python Type Casting

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

#### Calculations

Basic Arithmetic Operators for Python

![image.png](Programming%20notes.assets/image%20(8).png)

Python's operator precedence follows the BODMAS rule

![image.png](Programming%20notes.assets/image%20(9).png)



Basic incremental and decremental:

`x = x + 1` is the same as `x += 1`, increase x by 1

`x -= (y +7)` is the same as `x = x- (y + 7)`, reduce x value by (y +7)



Python also has built-in support for more complex math operations and functions such as trigonometric functions, logarithms and exponentiation.

![image.png](Programming%20notes.assets/image%20(10).png)

#### Data types

There are 4 different types of data types, Boolean, Number, Sequence and Mapping.



#### **Boolean Data Types**

Boolean is basically true and false.



#### **Numeric Data Types**

For numeric data types, there is the integer and float.

The difference between the two is that integers are whole numbers while floats are decimals.

**Integer**

`X = 50`

**Float**

`X = 50.0`



#### **Sequence Data Types**

There are 3 difference sequence data types, String, List and Tuple.



#### **String**

A string is a sequence of characters used to represent textual data. It can include letters, numbers, symbols and spaces.

You can display a string literal with the `print()` function:

`print("Hello")`

`print('Hello')`



#### **List**

A list is a collection which is ordered and changeable. It is used to store multiple items in a single variable. It also allows duplicate members.



![image.png](Programming%20notes.assets/image%20(11).png)

Use box brackets to create a list.

`newList = [1, 4, 6, 2]`

To determine how many values a list has, we can use `len()`.

   `print(len(newList))`

Lists are defined as class list.

Do note that the first position in a list is 0 not 1.



#### **Tuple**

- Tuples are like lists.
- Tuples can't be manipulated like lists (no append, extend or removal, basically as long as it affects the value in the tuple, it can't be done).
- You can use find and count elements in a tuple such as the `len(`) function in a tuple as it doesn't manipulate the tuple.
- Tuples are fast than lists as it is immutable (can't be changed).
- Use tuple if you do not plan on adding anything to a list.
- Tuple also uses normal brackets unlike lists.

   `newTuple = (1 ,2, 3, 4, 5)`

#### Mapping

**Dictionary**

- Dictionaries are used to store data values in key:value pairs.
- The main operation of a dictionary is to extract a value based on the key's name.
- Unlike lists, dictionaries use the keys to access it's members.
- Dictionaries can be used to sort, iterate and compare data.
- Dictionaries are created using braces {} with pairs separated with a comma and the key values associated with a colon.

`contact_num = {'John' : 98765432, 'Lois' : 87695432, 'Amy' : 92345678}`

- The keys in dictionaries must be unique, duplicate keys will result in rewriting of values.

`contact_num = {'John' : 98765432, 'Lois' : 87695432, 'Amy' : 92345678, 'Lois' : 12345678}`

`print(contact_num)`

Output:

`{'John': 98765432, 'Lois': 12345678, 'Amy': 92345678}`

- Only immutable objects (strings, etc) can be used for keys of a dictionary but either immutable or mutable objects can be used for the values of the dictionary.



**Mixing Data Types**

Python allows mixing data types in certain cases, such as concatenating strings or adding integers and floating-point numbers.



Combining two integer values will result in an integer value

Dividing two integer values will result in a float

Combining two float values will result in a float

Combining integer and float values will result in a float



---

Extra info:

Lists and tuples:

[https://www.youtube.com/watch?v=hANUgg72TDc&t=1s](https://www.youtube.com/watch?v=hANUgg72TDc&t=1s)

Dictionaries:

[https://www.youtube.com/watch?v=_4wOvc-vt4k](https://www.youtube.com/watch?v=_4wOvc-vt4k)

### Functions

#### print() Function

**String concatenation ("+" operator)**

String concatenation is the process of joining two or more character strings end-to-end to create a new, single string.

All variables must be converted to a string type using `str()` otherwise a runtime error will occur.

![image.png](Programming%20notes.assets/image%20(12).png)

**Comma operator (,)**

Used to print multiple value, such as string and integer together.

![image.png](Programming%20notes.assets/image%20(13).png)

A comma helps to insert a space before and after the value for you while a string concatenation would not.

**End parameter**

`end=` is a parameter used within the `print()` function to control what character is printed at the very end of the output.

![Screenshot 2026-05-09 161147.png](Programming%20notes.assets/Screenshot%202026-05-09%20161147.png)

**Sep parameter**

`sep=` is a keyword argument used in the `print()` function to define the character that separate multiple values in the output.

![image.png](Programming%20notes.assets/image%20(14).png)

**Backslash**

It provides a way to split a statement into multiple lines in your code editor.

It can also be used to insert characters that are illegal in a string, these are called Escape Characters.

![image.png](Programming%20notes.assets/image%20(15).png)

---

Extra:
[W3Schools.com](https://www.w3schools.com/python/gloss_python_escape_characters.asp)

##### Topic 2.2

#### print() Function

![image.png](Programming%20notes.assets/image%20(29).png)

The use of F-strings are for clarity and efficiency.

**What is print()?**

In python, print() is used to display output on the screen.

**F-strings (Python 3.6)**

**What is a F-string?**

A F-string is a way to insert values directly into a string.

`print(f"")`

> Uses `{}` to include values.

`print(f"{}")`

> It can contain arithmetic expressions.

![image.png](Programming%20notes.assets/image%20(16).png)

---

![image.png](Programming%20notes.assets/image%20(25).png)

> Placeholders can include format specifiers to control how many decimal places to be displayed.

> Add a format specifier after a colon (:) while inside the braces.

![image.png](Programming%20notes.assets/image%20(17).png)

> Use a percentage symbol to format a floating-point number as a percentage.

![image.png](Programming%20notes.assets/image%20(18).png)

Use a comma to display separator.

![image.png](Programming%20notes.assets/image%20(19).png)

![image.png](Programming%20notes.assets/image%20(20).png)

To display a value as a decimal integer, use the format specifier :d. (no decimal point)

![image.png](Programming%20notes.assets/image%20(21).png)

Format specifier can also include minimum field width, which is the minimum amount of spaces that should be used to display the values.

![image.png](Programming%20notes.assets/image%20(22).png)

![image.png](Programming%20notes.assets/image%20(23).png)

Use of <, ^ and > to control the alignment of text.

![image.png](Programming%20notes.assets/image%20(24).png)



---

When combining multiple specifiers, they must follow a specific order inside the curly braces.

`{ variable : [fill] [alignment] [width] [comma] [.precision] [type] }`

**.format() method (Python 3.0)**

- provides more flexibility
- create strings with placeholders enclosed in curly braces.

![image.png](Programming%20notes.assets/image%20(26).png)

The placeholders within the string will correspond to the named arguments provided in the `.format()` method.

![image.png](Programming%20notes.assets/image%20(27).png)

Just like F-strings, you can use a colon : inside the braces to apply "styles".

> Decimals: "{:.2f}".format(3.14159) → 3.14

> Commas: "{:,}". format(1000000) → 1,000,000

> Percentage: "{:.1%}".format(0.09) → 9.0%

![image.png](Programming%20notes.assets/image%20(28).png)

**String formatting "%" operator (Python 2.0 and older)**

`%s` stands for string and `%d` stands for decimal integer

![image.png](Programming%20notes.assets/image%20(30).png)

Additional formatting options like precision and width in the format specifiers such as `%.2` (2dp)

![image.png](Programming%20notes.assets/image%20(31).png)

| Specifier  | Data Type | Description                                 |
| ---------- | --------- | ------------------------------------------- |
| `%s`       | String    | Converts any object to a string using str() |
| `%d or %i` | Integer   | Displays whole numbers                      |
| `%f`       | Float     | Displays decimal numbers                    |

Injecting numbers between the % and the letter can control the layout.

`%10s` : Right-align in a field of 10 spaces

`%-10s` : Left- align in a field of 10 spaces

`%05d`: Pad a number with leading zeros until it is 5 digits long (eg. 00001)