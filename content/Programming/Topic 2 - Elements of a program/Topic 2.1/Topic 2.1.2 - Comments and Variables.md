# Comments and Variables

## Comments

"#" is a comment

Python will not execute lines that have "#" at the start of their line as they will not be part of the code.

We use comments to help us understand the code that we have written.

Example:

![image.png](Programming%20notes.assets/image%20(7).png)

This is so collaborators understand what is going on in the code. It is a good practice to comment your codes incase you get lost on your own.

## Variables

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



