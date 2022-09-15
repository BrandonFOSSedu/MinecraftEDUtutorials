# The String Data Type

## The String type in Typescript @showdialog

Typescript has several basic types, including a string type.

``let msg : string = "hello, world"``

In Minecraft, strings can be used as:
- Text output
- User chat commands
- Entity names
- Built-in functions

## Creating New Strings

To create new strings, use the ``let`` or ``const`` keyword followed by a variable name and a string type declartion. String literals are enclosed in "double" quotes or 'single' quotes.

``let myString : string = "I'm Mr. Murry"``
``const thisString : string = "Can't change me"``

### Exercise: Create two new string variables and assign them your first and last names.

```typescript
let firstName : string = "Mr."
let lastName : string = "Murry"
```

## Changing strings' values

String variables can change their value through later assignment statements, but the ``let`` statement should come first. 

``let newString : string = "abcd";``
``newString = "efgh";``
``player.say(newString);  // Outputs "efgh" to chat console``

*Constant* strings variables, created with the ``const`` keyword, cannot be changed after they are set.

``const myConst = "Can't change me"``
``myConst = "Err0R"  // An error will be raised for trying to change a const variable``

## String Literals and Variable Names

All programming code is made of text. Many programming languages use *string literals* enclosed in quotation marks to pass around string data. Typescript sees all other text in the source code as programming language keywords, numbers, and user defined types and names

Examples:
``"thisis-a=string"   // Single string literal``
``let a : number = 12  // Line of programming code``
``player.say("Howdy")  // Function with string literal input``
``"Put" + "Together"   // String expression``

*Variable names* have a few rules they follow
- First letter of the name must be a:
 - Upper or lower case letter
 - Underscore _
 - Dollar Sign $
- The next letters must be the same, but can include numeric digits
- Cannot use any reserved keywords, like let, player, etc...
- Cannot use spaces or whitespace (tabs, returns)
- Must be unique in current scope

Examples:
``let a_var = "string literal
let num1 = "Thirteen"
let 4lyfe  // Error: starts with digit
let let	   // Error: reserved keyword``


## String Expressions

Remember that *expressions* combine variables with operators and turn in to the result. Just like variable names, or identifiers, get *replaced* by their current values, expressions are replaced by their result.

``x = 36;
str = "Dear reader";
blocks.place(GRASS, pos(x, 0, 2*x - 12));
player.say(str + " this is Murry");``
``

First, the variable names are replaced by the contents of the variable.

``blocks.place( 1, pos( 36, 0, 2\*36 - 12));
player.say("Dear reader" + " this is Murry");``
``

Then every numeric or string expressions are evaluated and replaced with the result value.

``blocks.place( 1, pos( 36, 0, 60));  // 2*\36 - 12 turns into 60
player.say("Dear reader this is Murry");``  // Strings combined into 1
``
 
