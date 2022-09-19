
declare class Position {
/**
 * Returns a string representation of this position
 */
//% shim=.toString
public toString(): string;

/**
 * Adds the offset and returns a new position
 */
//% shim=.add
public add(offset: Position): Position;

/**
 * Creates a new world position by converting this position to a world position
 */
//% shim=.toWorldAsync promise
public toWorld(): Position;

/**
 * Gets the value of the specified coordinate: x, y or z
 * @param direction the axis for which to return the coordinate value
 */
//% shim=.getValue
public getValue(direction: Axis): number;

/**
 * Gets a value that indicates if the coordinate is relative to the user
 */
//% shim=.isRelative
public isRelative(direction: Axis): boolean;

/**
 * Returns a position moved by the given blocks
 */
//% shim=.move
public move(direction: CardinalDirection, blocks: number): Position;


## QueryTargetResult
//%
declare class QueryTargetResult {
//%
//% shim=.dimension
public dimension: number;

//%
//% shim=.yRot
public yRot: number;

//%
//% shim=.uniqueId
public uniqueId: string;

//%
//% shim=.x
public x: number;

//%
//% shim=.y
public y: number;

//%
//% shim=.z
public z: number;

}

## TargetSelector
class TargetSelector {
        /** * Sets the base coordinates for this target selector * @param p the coordinates at which this selector should be set */
        //% shim=.atCoordinate
        public atCoordinate(p: Position): void;

        /** * Sets the maximum distance from this selector's base coordinates * @param radius the maximum distance (in blocks) for this target selector, eg: 5 */
        //% shim=.withinRadius
        public withinRadius(radius: number): void;

        /** * Sets the minimum distance from this selector's base coordinates * @param radius the minimum distance (in blocks) for this target selector, eg: 10 */
        //% shim=.outsideRadius
        public outsideRadius(radius: number): void;

        /** * Adds a rule to this target selector * @param rule the rule to add, eg: "type" * @param value the value for the rule, eg: "chicken" */
        //% shim=.addRule
        public addRule(rule: string, value: string): void;

        /** * Returns a string containing the game notation for this target selector */
        //% shim=.toString
        public toString(): string;

    }

