# Creating a Calculator

```template
let a : number = 0      // The Accumulator variable

let sa : string = "sa"  // Text to type in chat console
let ga : string = "ga"
let ra : string = "ra"
let aa : string = "adda"
let suba : string = "suba"

function setA(n: number)
{ 
    a = n
}

function getA()
{ 
    player.say(a)
}

function resetA()
{ 
    a = 0
}

function addA(n: number)
{ 
    a = a + n 
}

function subtractA(n: number)
{ 
    a = a - n
}

// Event-driven commands wait for chat strings,
// then call the handle function
player.onChat(sa,    // sa n
              setA)
player.onChat(ga,    // ga
              getA)
player.onChat(ra,    // ra
              resetA)
player.onChat(aa,    // adda n
              addA)
player.onChat(suba,  // suba n
              subtractA)
```

## Using the Interactive Calculator @showdialog

In this lesson, you will use and modify a simple 4-function calculator. The starter code includes a variable ``a``, which we will call the accumulator. This accumulator remembers the result of the previous calculation, so that you can perform additional operations.  

You will type out special commands in the Minecraft chat window to see how the calculator works. Right now, you can only add and subtract with an accumulator variable.

## Interactive Chat Commands

In order to make Minecraft coding more engaging, *event* commands to let the user call any function. 

Makecode provides a built-in set of event-driven functions, like ``player.onChat()``. This calculator uses ``player.onChat()`` to call the calculator's functions.

### Exercise: Practice using the commands below in the chat console.

- "ga"       => Prints out the value of the accumulator
- "sa *n*"   => Assigns an additional numeric value to the accumulator
- "ra"       => Resets the value of the accumulator to zero
- "adda *n*" => Adds a user-defined value *n* to the accumulator
- "suba *n*" => Subtracts user-defined value *n* to the accumulator

## Multiply and Divide

So far, the calculator can perform two mathematical operations. Typescript can perform several additional operations with variables and in expressions.

You are going to write some new ``player.onChat()`` commands that implements multiplication and division. To save space, we are going to write both the ``onChat`` command and function definition in the same statement.

Example: 
- ``player.onChat("mula", function mulA(n : number) { ... } )``
- ``player.onChat("diva", function divA(n : number) { ... } )``

### Exercise: Create multiply and divide onChat commands. Use the examples above and fill in the missing code for both functions.

```typescript
player.onChat("mula", 
              function mulA(n : number) 
              { 
                  a = a*n
              } 
)

player.onChat("diva", 
              function divA(n : number) 
              { 
                  a = a/n 
              }
)
```

## Adding some text output

Most of the calculator's functions are silent. It would be helpful to see the results of our chat commands as we type them.

By adding ``player.say()`` commands inside each function's code , we can write helpful messages back to the user. 

Examples:

- ``function setA(n : number) {``
- ``    a = n;``
- ``    player.say("Set the value of a to " + n); }``
- ``function getA() {``
- ``    player.say("The current value of a is " + a); }``
- ``function addA(n : number) {``
- ``    a = a + n;``
- ``    player.say("The result is " + a); }``

### Exercise: Copy the changes to the example functions, and add say commands to tell the user the result of the remaining functions

```typescript
function resetA() 
{
    a = 0;
    player.say("The accumulator has been reset to 0");
}

function mulA(n : number)
{
    a = a*n
    player.say("The result is " + a);
}

function divA(n : number) 
{
    a = a/n;
    player.say("The result is " + a);
}
```

## Printing the results in big block letters

Wouldn't it be cool if we could see our calculator work out in the Minecraft world? Typing and reading from the chat console doesn't include anything unique about Minecraft.

Let's try to use some of Makecode's built-in functions to have our calculator commands show up in the outside world.

Add the following code to the end of the rest of the functions. Then test out all your chat commands.

``blocks.print(a.toString(), DIAMOND_BLOCK, pos(5, 0, 5), WEST)``

```typescript
function mulA(n : number) 
{
    a = a*n;
    player.say("The result is " + a);
    blocks.print(a.toString(), DIAMOND_BLOCK, pos(5, 0, 5), WEST); // Here!
}
```
