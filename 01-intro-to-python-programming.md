# 1 - Intro to Python Programming

## Chapter 01 - Variables, Expressions, and Statements

### Values and Types 

A _value_ is one of the basic things a program works with, such as a letter or number.

Values come in different _types_, such as:
- **String** - 'Hello, Earthlings' or "Hi, Aliens!"
- **Integer** - 420
- **Float** - 6.9
- **Boolean** - True / False

You can check the type by using _type()_ fuction:
```
name = 'Jungkook'
type(name)

<class 'str'>
```

### Variables

A _variable_ is a name that refers to a value.

An _assignment statement_ creates new variables and gives them values.
```
message = "I love lamp."
lamp_love = 9000
x = 44.7
```

### Statements

A _statement_ is a section of code that represents a command or action.

### Operators and Operands

_Operators_ are special symbols that represent computations like addition and multiplication.

Python follows mathematical convention...aka _PEMDAS_!

_Operands_ are the values that the operator is applied to.

- `+`
- `-`
- `*`
- `/` (division returns a float)
- `//` (division that truncates the result to an integer)
- `**`
- `%` modulus

### Expressions

An _expression_ is a combination of values, variables, and operators.

An expression is _evaluated_ when it's simplified by performing the operations to field a single value.
```
1 + 1
>> 2
```

### Modulus operator

Useful to:
- determine even vs. odds
- check whether one number is divisible by another
- extract the right-most digit of digits from a number

### String operations

The `+` and `*` operators also work for strings.

String _concatenation_ means to join the strings together.

```
a = 'butt'
b = 'face'

print(a+b)

>> buttface
```

```
hobby = 'shots '
print(hobby * 3)

>> shots shot shots
```

### Asking the user for input

The `input()` function gets user input from the keyboard.

It can be empty, but it's helpful to pass a string into the input function.

```
fav_toy = input('What is your favorite toy? ')

What is your favorite toy? ball

print(fav_toy)
>> ball
```

If you expect the user to type an integer, you can try to convert the return value to int using the _int()_ function.

### Comments

```
# Comments can be added to an entire line.
Or not. # They could also be added to the END of a line.
```
Comments are most useful when they document _non-obvious_ features of the code, such as to explain _why_.


## Chapter 02 - Conditional Execution

### Boolean expressions

A _boolean expression_ is an expression that is either `True` or `False`. 

`True` and `False` are special values that belong to the class `bool`.

### Logical operators

There are three logical operators: `and`, `or`, and `not`.

| Operator  | Description  | Example |
|-----------|--------------|------------|
| `and`     | Returns `True` if both statements are true	     | x < 5 and  x < 10        |
| `or`      | Returns `True` if one of the statements is true	  | x < 5 or x < 4      |
| `not`     | Reverse the result, returns `False` if the result is true	 | not(x < 5 and x < 10) |	
     
### Conditional execution

A _conditional statement_ controls the flow of execution depending on some condition.

```
if x > 0 :
    print('x is positive')

>> x is positive
```
If the logical condition is true, then the indented statement gets executed. If the logical condition is false, the indented statement is skipped.

Occasionally, it is useful to have a body with no statements (usually as a placeholder for code you haven’t written yet). In that case, you can use the `pass` statement, which does nothing:

```
if x < 0 :
    pass    # A placeholder line that does nothing
```


### Alternative execution

A second form of the `if` statement is _alternative execution_, in which there are two possibilities and the condition determines which one gets executed.

```
if x%2 == 0 :
    print('x is even')
else :
    print('x is odd')
```

### Chained conditionals

_Chained conditionals_ are a conditional statement with a series of alternative branches.

```
if x < y:
    print('x is less than y')
elif x > y:
    print('x is greater than y')
else:
    print('x and y are equal')
```
`elif` is an abbreviation of “else if.” 

Again, exactly one branch will be executed. 

There is no limit on the number of elif statements. If there is an else clause, it has to be at the end, but there doesn’t have to be one.

Each condition is checked in order. If the first is false, the next is checked, and so on. If one of them is true, the corresponding branch executes, and the statement ends. Even if more than one condition is true, only the first true branch executes.

### Nested conditionals

A _nested conditional_ is a conditional statement that appears in one of the branches of another conditional statement.

```
if x == y:
    print('x and y are equal')
else:
    if x < y:
        print('x is less than y')
    else:
        print('x is greater than y')
```
The outer conditional contains two branches. The first branch contains a simple statement. The second branch contains another `if` statement, which has two branches of its own. 

Avoid nested conditionals when possible. Opt for simpler code.

This:

```
if 0 < x:
    if x < 10:
        print('x is a positive single-digit number.')
```

can be rewritten as:
```
if 0 < x and x < 10:
    print('x is a positive single-digit number.')
```


### Catching exceptions using try and except

There is a conditional execution structure built into Python to handle certain errors. 

The idea of `try` and `except` is that you know that some sequence of instruction(s) may have a problem and you want to add some statements to be executed if an error occurs. These extra statements (the except block) are ignored if there is no error.

```
inp = input('Enter Fahrenheit Temperature:')
try:
    fahr = float(inp)
    cel = (fahr - 32.0) * 5.0 / 9.0
    print(cel)
except:
    print('Please enter a number')
```

Python starts by executing the sequence of statements in the `try` block. If all goes well, it skips the `except` block and proceeds. If an exception occurs in the `try` block, Python jumps out of the `try` block and executes the sequence of statements in the `except` block.
```
Enter Fahrenheit Temperature: 72
>> 22.22222222222222
```
```
Enter Fahrenheit Temperature: fred
>> Please enter a number
```
Handling an exception with a `try` statement is called _catching_ an exception. In this example, the `except` clause prints an error message. In general, catching an exception gives you a chance to fix the problem, or try again, or at least end the program gracefully.

### Short-circuit evaluation of logical expressions

It is called _short-circuiting_ when Python is part-way through evaluating a logical expression and stops the evaluation because Python knows the final value for the expression without needing to evaluate the rest of the expression.

The short-circuit behavior leads to a technique called the _guardian pattern_, where we construct a logical expression with additional comparisons to take advantage of the short-circuit behavior.


## Chapter 03 - Functions

## Chapter 04 - Loops and Iterations

## Chapter 05 - Strings

## Chapter 06 - Lists

## Chapter 07 - Dictionaries

## Chapter 08 - Tuples

## Chapter 09 - Sets

## Chapter 10 - Sequence Functions

## Chapter 11 - Object-oriented Programming
