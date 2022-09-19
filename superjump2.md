# Super Jump part 2


## Create a String Variable
Create a string variable for the chat command.

``let cmd : string = "jump"``

```typescript
let cmd : string = "jump"
```

## Create a Function
Create a Function named jump with no inputs.

``function jump() {

}``

```typescript
function jump() {

}
```

## Add teleport command
Add a ``teleport`` command inside of the body of the ``jump`` function. Change the 2nd input of the ``pos`` function.

``player.teleport(pos(0, 10, 0))``

```typescript
function jump() {
    player.teleport(pos(0, 10, 0))
}
```

## Create an onChat command
Now create an ``onChat`` command. The ``onChat`` command takes 2 inputs, a string and a function.

``player.onChat(cmd, jump)``

```typescript
player.onChat(cmd, jump)
```

## Test your code
Go into Minecraft and open the chat window with the 't' or 'Enter' keys. Then type "jump".

## Adding user input
Right now, the jump function always teleports the player a set number of blocks into the air.

Let's add an input to our jump function so that we can interactively determine how high the player teleports.

Then, in the ``pos`` function, set the 2nd input to the height variable.

```typescript
function jump (height : number) {
    player.pos(0, height, 0)
}
```

## Giving inputs to onChat
In Minecraft chat, we first type the string that will activate the ``onChat`` command, then we type a space, and then a number that our function will use to teleport the player.

``jump 40``

Open up the Minecraft chat and experiment with the new way of running the ``onChat`` command.

## Comment out your code
We are going to rewrite the program to be a little more compact.

Command out all the code we have written so far by putting a ``/*`` before, and a ``*/`` after.

```typescript
/*
...
*/
```

## Rewriting the program
Start by pulling an ``onChat`` command from the toolbox. Notice how instead of using variables, Makecode has prepopulated the command for us.

Change the first parameter to "jump" to match our code from before.

Next, add a ``player.teleport`` *inside* the function block. Again, change the 2nd parameter of the ``pos`` function to a different value.

Test your code to make sure it works.
```typescript
player.onChat("jump", function() {
    player.teleport(pos(0,10,0))
})
```

## Adding back the height input
We still want to be able to determine how high the player gets teleported.

Add a ``height`` variable *inside* our function definition that is *within* the ``onChat`` parenthesis.

``player.onChat("jump", function(height : number) ...``

Next, change the 2nd parameter of the ``pos`` function to ``height``. Test your code.

```typescript
player.onChat("jump", function(height : number) {
    player.teleport(pos(0, height, 0))
})
```
