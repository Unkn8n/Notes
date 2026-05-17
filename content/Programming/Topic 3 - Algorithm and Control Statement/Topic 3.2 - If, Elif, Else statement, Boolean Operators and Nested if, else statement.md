# "If" statement

An "If" statement is written by using the `if` keyword.
After an `if` , should there be any more conditions, you can add on using an `elif` (Else if) or/and an `else` . 
The `elif` is like python's way of saying "if the previous conditions aren't true, then try this condition." While the `else` is if all the conditions return as false.

# Boolean Operators

![[BooleanOperators.png]]

The `and` and `or` operators are used to combine conditional statements.

The `not` operator is used to invert a condition.

# Nested if, else statement

A nested `if` is when you have an `if` statement inside another `if` statement.
Since `if` statements cannot be empty, use the `pass` statement to move on without getting an error.

In a nested `if` statement, the inner `if` must be indented otherwise you will get an `IndentationError`.

A nested `if` is still an `if` so it has to fulfill the outer `if` condition before it can go to the inner `if` condition. 
![[ifelifelse.png]]