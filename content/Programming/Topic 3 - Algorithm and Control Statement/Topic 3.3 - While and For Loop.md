# While and For Loop

A loop statement allows us to execute a statement or groups of statements.

Below is an example of a loop in a flowchart.
![[LoopFlowchart.png]]

## While Loop

While Loops are used to execute a block of statements repeatedly until a given condition is satisfied.

When the condition becomes false, the line immediately after the loop in the program will be executed.

```
count = 1
while count < 4:
	print(count)
	count += 1
```
```
Output:
1
2
3
```

## For Loop

A For loop is used for iterating over  a sequence (list, tuple, dictionary, set or string).

For loops are used to loop through an iterable object and perform the same action for each entry.

Printing each name in the name list:
```
names = ['Tom', 'Dick', 'Harry']
for name in names:
	print(name)

Output:
Tom
Dick
Harry

```

A For loop that iterates every character in a string:
```
str = 'Python'
for character in str:
	print(character.upper())

Output:
P
Y
T
H
O
N
```

A For Loop to loop though a set of codes a specific number of times using the range() function.
The range() function returns a sequence of numbers, starting from 0 by default and increments by 1 by default and will end at a specified number.

```
for x in range(6):
	print(x)

Output:
0
1
2
3
4
5

for x in range(2,6):
	print(x)

Output:
2
3
4
5
```

Let's say you want to add numbers before a name and have the names be in uppercase.

```
friends = ['John', 'Alex', 'Pete']  
for i in range(len(friends)):  
    print(f"{i + 1}. {friends[i].upper()}")

Output:
1. JOHN
2. ALEX
3. PETE
```
## Break statement

- The `break` statement is used when you need to exit a loop when an external condition is triggered or when you want to skip a part of the loop and start the next line for execution.
- It terminates the current loop and executes the next statement.
- It can be used for both while and for loops.

```
num = 10
while num > 0:
	print('Number: ', num)
	num -= 1
	if num == 5:
		break
print(f'Number is {num}')

Output:
Number:  10
Number:  9
Number:  8
Number:  7
Number:  6
Number is 5
```

Using break statement in a For loop
With the break statement we can stop the for loop before it has looped though all the items.

```
items = ['pc', 'mouse', 'keyboard', 'adaptor', 'monitor']
for i in items:
	print(i)
	if i == 'keyboard':
		break

Output:
pc
mouse
keyboard
```

## Continue statement

The `continue` statement returns the control to the beginning of the loop. It terminates all the remaining statements in the current iteration of the loop and moves the control back to the top of the loop. 
The `continue` statement can be used in both while and for loop.

```
count = 0
while (count < 6):
	count += 1
	if count == 3:
		continue
	print(count)

Output:
1
2
4
5
6
```

```
for letter in "Python":
	if letter == "h":
		continue
	print(f'Current letter is {letter}')
	
Output:
Current letter is P
Current letter is y
Current letter is t
Current letter is o
Current letter is n
```

## Nested For loops

A loop inside another loop is called a nested loop.
The inner loop will be executed for each iteration of the outer loop.

#### How it works:
- The program first encounters the outer loop, executing the first iteration.
- The first iteration triggers the inner nested loop which then runs to completion.
- Then the program returns back to the top of the outer loop, completing the second iteration and then triggering the nested loop again.
- The nested loop runs to completing and the program returns back to the top of the outer loop until the sequence is completed.

```
num_list = [1,2,3]
alph_list = ['a', 'b', 'c']

for number in num_list:
	print(number)
	for letter in alph_list:
		print(letter)

Output:
1
a
b
c
2
a
b
c
3
a
b
c
```