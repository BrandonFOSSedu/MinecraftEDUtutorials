# Using Functions


```template
// Using Functions
// Call Makecode functions, and user-defined function


// Step 1: Calling Makecode Functions 
player.teleport( pos(0, 0, 0))
blocks.place( GRASS,
              pos(0, 0, 0))
mobs.spawn( MUSHROOM_COW, 
            pos(0, 0, 0))
gameplay.toggleDownfall()
agent.teleportToPlayer()
gameplay.setGameMode( SURVIVAL,
                      mobs.target(LOCAL_PLAYER))
    

// Drag some code blocks into the editor




// Calling user-defined functions
function oops() 
{
    gameplay.setGameMode( SURVIVAL,
                          mobs.target(ALL_PLAYERS))
    gameplay.setGameMode( CREATIVE,
                          mobs.target(LOCAL_PLAYER))
    mobs.kill( mobs.target(ALL_ENTITIES))
}

function goHome() 
{
    mobs.spawn( MUSHROOM_COW, pos(0, 0, 0))
    gameplay.setGameMode( CREATIVE, mobs.target(LOCAL_PLAYER))
    blocks.fill( DIRT, pos(5, -1, 5), pos(-5, 5, 5), FillOperation.Replace)
    blocks.fill( DIRT, pos(5, -1, 5), pos(5, 5, -5), FillOperation.Replace)
    blocks.fill (DIRT, pos(-5, -1, -5), pos(-5, 5, 5), FillOperation.Replace)
    blocks.fill( DIRT, pos(-5, -1, -5), pos(5, 5, -5), FillOperation.Replace)
    blocks.fill( DIRT, pos(-5, 6, -5), pos(5, 6, 5), FillOperation.Replace)
}

function showBlocks() 
{
    player.say("Spawning blocks in a row");
    for (let i: number = 0; i <= 400; i++) 
    {
            blocks.place(i, pos(i, 0, 0))
    }
}

// Call the functions below



// New onChat commands

player.onChat("blocks", showBlocks);

player.onChat("home", goHome);

player.onChat("anon", 
              function()
              {
                  player.say("Running anonymous function");
                  agent.teleportToPlayer();
              }
)	
player.onChat("sus", 
              function() 
              {
	          player.say("Sussy agent...");
              }
)

// Type the commands in the chat console



// Creating new event-driven commands
```

## Practice
Run the functions

```typescript
goHome();
```
