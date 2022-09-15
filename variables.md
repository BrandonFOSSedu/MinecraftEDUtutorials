# Minecraft Education Edition Tutorials - Event Driven Commands

```template
// This is a comment. You'll be putting your code underneath here.
```

## Variables and Data @showdialog

The Typescript language is based on Javascript, but with additional support for static data types and error checking.

Today we will take a look at some of the basic types of Typescript and how to use variables in Minecraft programming.

## Creating variables

Typescript lets users create variables using the ``let`` keyword, followed by a user defined *identifier*.

An identifier is a *name* for a variable. Once given a value, variables can be used in other parts of the program where the name will be replaced by the current value of the variable.

Example: ``let x : number = 2``

### Exercise: Create 2 variables with the type *number* and *assign* each a numeric value.

```typescript
let x : number = 2
let y : number = 3
```

## Print your variable

Once we have a variable with a value, we can use the ``player.say()`` function to print out the value.

### Exercise: Write 2 ``player.say()`` statements to output the values of variables x and y.

```typescript
player.say(x);
player.say(y);
```
## Changing the value of a variable

Unlike in Algebra, variables in programming are not *unknowns* waiting to be solved for. All usage of variables in programming follow the rule of *substitution*. Each occurrence of a user defined variable will be substituted for it's value.

Also unlike Algebra, variables do not need to retain their value throughout a program. Variables can be *reassigned* through additional assignment statements: ``x = 10``.

### Exercise: After the previous code, write additional assignment statements and print out the new values with ``player.say()`` statements.

```typescript
x = 20
y = 10
player.say(x)
player.say(y)
```

## Defining Expressions

Most programming languages allow users to write *mathematical expressions*, just like you might in a math class: ``3*x - 2*y``.

Typescript will perform the substitutions of each variable in an expression, and then *evaluate* the expression using the same *order of operations* from math class.

Table of Mathematical Operator Symbols
- + Addition
- - Subtraction
- * Multiplication
- / Division
- ** Exponentiation
- % Modulus (remainder)
- ++ Plus 1
- -- Minus 1

## Using Expressions

Let's practice using expressions.

### Exercise: Let's create a new variable, z, and assign it to the result of an expression involved the previous 2 variables.

```typescript
let z = 4*x - y/2
player.say(z)
```

## Using Expressions Part 2

Typescript will substitute variables and evaluate expressions *anywhere* in code, not just in assignment statements. For example, we can put expressions *inside* the parentheses of our ``player.say()`` statements, and the result of of expression will be output. Think about this like order of operations (PEMDAS). The expression inside the parenthesis takes place first.

### Exercise: Write 3 more ``player.say()`` statements using expressions inside the parentheses. 

```typescript
player.say(x+y+z)
player.say(z**x/y)
player.say( (z - x)/y )
```

## Defining Functions

Variables are useful for storing data that can be used later. Just like in Algebra, programming languages also let users define *functions*. Functions are useful for storing *code* that can be reused later. Function definitions, like variables, typically involve a *name*, but are defined within a *block of code*.

Example:

``function sayX() {

	player.say(x)

}``

### Exercise: Define a function named sayVars() that output the value of the three variables created so far

```typescript
function sayVars() {
	player.say(x)
	player.say(y)
	player.say(z)
}
```

## Using functions

Notice that the function did not actually *execute* from the previous step. In order to execute the function, we need to write an expression statement that *calls* the function.

### Exercise: On an empty line after the function definition, write the name of the function and it's empty parentheses

```typescript
function sayVars() {
	player.say(x)
	player.say(y)
	player.say(z)
}

sayVars()
```
