# Target Selector Mechanics

## Gamemode Functions
function setGameMode(mode: GameMode, player: TargetSelector): void;
function xp(amount: number, target: TargetSelector): void;
function title(target: TargetSelector, title: string, subTitle: string): void;

## Player Functions
function tell(target: TargetSelector, message: any)

## Mobs Functions
export function queryTarget(target: TargetSelector): QueryTargetResult[] {
    return _queryTargetCore(target);
}
function effect(effect: Effect, target: TargetSelector, duration?: number, amplifier?: number): void;
function applyEffect(effect: number, target: TargetSelector, duration?: number, amplifier?: number): void;
function clearEffect(target: TargetSelector): void;
function give(target: TargetSelector, block: number, amount: number): void;
function teleportToPosition(target: TargetSelector, destination: Position): void;
function teleportToPlayer(target: TargetSelector, destination: TargetSelector): void;
function enchant(target: TargetSelector, spell: string, level: number): void;
function kill(target: TargetSelector): void;
function execute(target: TargetSelector, position: Position, command: string): void;

function target(kind: TargetSelectorKind): TargetSelector;
function near(target: TargetSelector, pos: Position, radius: number): TargetSelector;
function entitiesByType(type: number): TargetSelector;
function playerByName(name: string): TargetSelector;
function playersInGameMode(mode: GameMode): TargetSelector;
function parseSelector(str: string): TargetSelector;


function _queryTargetCore(target: TargetSelector): QueryTargetResult[];



