# Data types

There are 4 different types of data types, Boolean, Number, Sequence and Mapping.



## Boolean Data Types

Boolean is basically true and false.



## Numeric Data Types

For numeric data types, there is the integer and float.

The difference between the two is that integers are whole numbers while floats are decimals.

**Integer**

`X = 50`

**Float**

`X = 50.0`



## Sequence Data Types

There are 3 difference sequence data types, String, List and Tuple.



#### String

A string is a sequence of characters used to represent textual data. It can include letters, numbers, symbols and spaces.

You can display a string literal with the `print()` function:

`print("Hello")`

`print('Hello')`



#### List (Topic 5.1)

A list is a collection which is ordered and changeable. It is used to store multiple items in a single variable. It also allows duplicate members.



![image.png](Programming%20notes.assets/image%20(11).png)

Use box brackets to create a list.

`newList = [1, 4, 6, 2]`

To determine how many values a list has, we can use `len()`.

   `print(len(newList))`

Lists are defined as class list.

Do note that the first position in a list is 0 not 1.



#### Tuple (Topic 5.1)

- Tuples are like lists.
- Tuples can't be manipulated like lists (no append, extend or removal, basically as long as it affects the value in the tuple, it can't be done).
- You can use find and count elements in a tuple such as the `len(`) function in a tuple as it doesn't manipulate the tuple.
- Tuples are fast than lists as it is immutable (can't be changed).
- Use tuple if you do not plan on adding anything to a list.
- Tuple also uses normal brackets unlike lists.

   `newTuple = (1 ,2, 3, 4, 5)`

## Mapping

#### Dictionary

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



## Mixing Data Types

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

