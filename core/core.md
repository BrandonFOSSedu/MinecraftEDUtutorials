# Minecraft Makecode Core

A list of Minecraft Makecode's API

## Namespaces

- player
- mobs
- blocks
- agent
- position
- builder
- console
- control
- Array
  - function isArray(obj: any): boolean;
- Math
- Object
  - function keys(obj: any): string[];
- String
  - function fromCharCode(code: number): string
- StringMap
- __internal


## Classes

- ChatCommandArgs
- TargetSelector
- QueryTargetResult 

## Functions

- pos(x: number, y: number, z: number): Position 
- posLocal(x: number, y: number, z: number): Position
- posCamera(x: number, y: number, z: number): Position
- world(x: number, y: number, z: number): Position 
- world(x: number, y: number, z: number): Position 
- parseFloat(text: string): number;
- parseInt(text: string, radix?: number): number 
- randint(min: number, max: number): number;
- isNaN(x: number) 


## Interfaces

- Array<T>
- Boolean
- Function
- IArguments
- Number
  - toString(): string;
- Object
- RegExp


## Types

- TemplateStringArray
- uint8, uint16, uint32
- int8, int16, int32
- Action = () => void


## Constants
- NaN = 0 / 0
- Infinity = 1 / 0


## Enums
- Block
- Item
- TravelMethod
- TestForBlocksMask 
- CloneMask
- CloneMode
- TargetSelectorKind
  - NearestPlayer, LocalPlayer, RandomPlayer, AllPlayers, AllEntities, MyAgent
- Axis
- SixDirection
- FourDirection
- TurnDirection
- CardinalDirection
- CompassDirection
- AnimalMob
- MonsterMob
- ProjectileMob
- Effect
- AgentCommand
- AgentDetection
- AgentInspection
- BlockColor
- GameMode
- Weather
- DayTime
- FillOperation
- GameRule
- GameDifficulty
- AgentAssist
- TimeQuery
- LeverPosition
- ComparatorMode
- ShapeOperation
- ChatArgument
- ColoredBlock
