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

A _statement_ is a unit of code that the Python interpreter can execute.

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

## Chapter 03 - Functions

## Chapter 04 - Loops and Iterations

## Chapter 05 - Strings

## Chapter 06 - Lists

## Chapter 07 - Dictionaries

## Chapter 08 - Tuples

## Chapter 09 - Sets

## Chapter 10 - Sequence Functions

## Chapter 11 - Object-oriented Programming
