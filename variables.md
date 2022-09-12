# Minecraft Education Edition Tutorials - Event Driven Commands

```template
let a : number = 10
let s : string = "Hello World"
let b : boolean = true
```

## Variables and Data @showdialog

The Typescript language is based on Javascript, but with additional support for static data types and error checking.

Today we will take a look at some of the basic types of Typescript and how to use variables in Minecraft programming.

## Creating variables

Typescript lets users create variables using the ``let`` keyword, followed by a user defined *identifier*.

An identifier is a *name* for a variable. Once given a value, variables can be used in other parts of the program where the name will be replaced by the current value of the variable.

```typescript
let x : number = 2
let y : number = 3
```

## Print your variable

Once we have a variable with a value, we can use the ``player.say`` function to print out the value.

```typescript
player.say(x);
```

## Something is wrong!

Hover your cursor over the ``say`` method and note the *type* of the message. Typescript requires that any variables we use or give to functions must be the correct type. What type does ``x`` have?

We need a way to *convert* the number into a *string* variable. Luckily, Typescript allows us to convert a number into a string with the ``.toString()`` method.

```typescript
player.say(x.toString())
```
