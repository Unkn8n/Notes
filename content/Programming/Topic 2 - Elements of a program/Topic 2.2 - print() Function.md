# print() Function

![image.png](Programming%20notes.assets/image%20(29).png)

The use of F-strings are for clarity and efficiency.

**What is print()?**

In python, print() is used to display output on the screen.

## F-strings (Python 3.6)

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

## .format() method (Python 3.0)

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

## String formatting "%" operator (Python 2.0 and older)

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