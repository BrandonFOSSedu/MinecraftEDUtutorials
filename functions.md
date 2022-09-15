# Introduction to Functions

```template
let a : number = 12;
let b : number;
```

## Variables Review

We use the ``let`` keyword to declare a new variable, the ``:`` symbol to give a *type*, and the ``=`` operator to *assign* the variable a value.

## Uninitialized Variables

To output the value of a variable in Makecode, we use the ``player.say()`` command. Let's see what happens when we try to output the two variables ``a`` and ``b``.

### Exercise: Output the value of the two variables.

```typescript
player.say(a);
player.say(b);
```

## Function Inputs

So far, all of the code we have written is executed as soon as the green play button is pressed. We can use *functions* to change aspects of our program using Minecraft's built-in *event handlers*. But first, we need a function that will assign a value to ``b``.

Just like in Algebra class, we can create a function that takes *inputs*, and then use that input in the code body of the function.

Example:

``

function setB(num1 : number) {

...

}

``


### Exercise: Create a function named ``setB()`` that takes one numeric input, ``num1`` and assigns variable ``b`` to it.

```typescript
function setB(num1 : number) {
	b = num1;
}
```

## Calling a User Defined Function

The function definition from the previous step does not actually *execute* the function; we have to now *call* the function in order to use it.

Example: ``setB(12)``

### Exercise: Call function ``setB()`` with a numeric input, and then output the new value of ``b``.

```typescript
setB(20);
player.say(b)
```

## Variable Scope

All variables in Typescript have a *scope*, or visibility. So far, all of our code has been executing in the *global scope*. This means that any variables or functions defined outside of any other function are visible (in scope) anywhere else in the program. That's why the ``setB()`` function was able to see and use variable ``b``.

Function ``setB()`` included it's own *local variable*, ``num1``. If we try to use ``num1`` outside of ``setB()`` (global scope), the compiler will throw an error.

### Exercise: Add a new ``player.say()`` statement to output ``num1`` *outside* the ``setB()`` function body.

```typescript
player.say(num1)
```

## Get and Set Functions

It is common to create functions that will *get* or *set* variables. We have already created a function ``setB()`` that assigns a value to B. Let's create a new function that will *get* the value and output it with a ``player.say()`` statement.

Since a *get* function just needs to output a global variable, it does not need any input variable parameters inside it's parenthesis.

### Exercise: Define a new function ``getB()`` that output the value of ``b``. Then, call ``getB()`` to make sure it works.

```typescript
function getB() {
	player.say(b)
}

getB();
```

## Get and Set part 2

Now that we can get and set variable b, let's define 2 new functions to do the same for variable ``a``.

### Exercise: Define functions ``setA()`` and ``getA()`` and call them.

```typescript
function setA(num1 : number) {
	a = num1;
}

setA(-5);

function getA() {
	player.say(a);
}

getA();
```

## Event Driven Programming

So far, all of code is non-interactive. Minecraft Makecode does not have standard *input* commands like most other programming environments. Instead, Minecraft Makecode uses *event driven* commands to trigger functions based on an event in the game.

When we worked in the block-based environment, we got used to the *onChat* style commands. Let's create a new ``player.onChat()`` command that let's us call our get and set functions. See below for an example of how to create an ``onChat()`` statement that uses our functions.

``player.onChat("setmyvar", setA);``

The ``onChat()`` command takes 2 inputs. The first, ``"setmyvar"``, is the text the user needs to type in the chat window to trigger the ``onChat()`` command. The second input, ``setA``, is the *name* of the function to call when the correct text is typed. Notice, we only give the *name* of the function, we do not include the parenthesis *or* it's input.

With this code, if we were to type "setmyvar" in chat followed by a number, Makecode will see execute the ``onChat()`` command and give the number to the ``setA()`` function.

## Input and Output with ``onChat()``

Now it's time to put everything together. We need to create 4 ``player.onChat()`` statements, one for each get and set function for our two variables.

Example: ``player.onChat("seta", setA);``

### Exercise: Write the 4 ``player.onChat()`` commands that use the 4 functions, ``setA``, ``getA``, ``setB``, and ``getB`` that were created above.

```typescript
player.onChat("seta", setA);
player.onChat("geta", getA);
player.onChat("setb", setB);
player.onChat("getb", getB);
```

## Use Your Functions!

Go into chat and practice using the ``onChat()`` commands to change and output the values of variables ``a`` and ``b``.
