# Chapter 2: Expanding Your Syntax Game

This chapter will focus on teaching the most important argument datatypes, and the way to do that is to teach other commands.

## Selectors, Coordinates, and the `tp` command

The `tp` command sets the position of one or more entities to either a specific coordinate, or that of another entity. You are also able to set rotation. The `tp` command is much more complex than the `say` command, which we went through in Chapter 1.  Here is *some* of its syntax:
```
/tp <location>
/tp <destination>
/tp <targets> <location> [<rotation>]
/tp <targets> <destination> [<rotation>]
```
There's a **lot** to explain here. First off, there's *multiple* ways of writing this command, where each method does something slightly different. Now let's explain what each of these lines do:
- `/tp <location>` teleports you to a specific world coordinate;
- `/tp <destination>` teleports you to a specifc entity;
- `/tp <targets> <location> [<rotation>]` teleports all of the target entities to a specfic world coordinate, with optional rotation data; and
- `/tp <targets> <destination> [<rotation>]` teleports all of the target entities to a specfic entity, with optional rotation data.

Now let's explain what each *argument* does:
- `<location>` expects a coordinate datatype;
- `<targets>` expects an entity datatype;
  - `<destination>` also expects an entity, but can only select **one** entity; and
- `<rotation>` requires a rotation datatype

We can separate the next section into 3 parts: *Target Selectors*, *Coordinates* and *Rotation*. Each of these is an important *datatype*, but the latter isn't as important right now.

### Target Selectors
>[!NOTE]
>
> To clear potential confusion later on, players are entities like how zombies, skeletons and others are.

Target selectors are part of a more broad entity datatype. This datatype is what the `<targets>` and `<destination>` arguments refer to, and are how entities are selected with commands. If no entities are selected, then the argument (and consequently the command) will fail.

The entity datatype can accept either a player's username, an entity's UUID (UUIDs aren't important till *far* later on), **or** one of 6 target selectors, which select different entities depending on which one is used:
- `@a`, which selects all players;
- `@e`, which selects all entities;
- `@p`, which selects the nearest player;
- `@n`, which selects the nearest entity;
- `@r`, which selects a random player; or
- `@s`. For now, think of it as selecting yourself. The true definition will be explained in the later parts.

But that isn't all. You can also specify additional arguments to filter entities that meet certain criteria, called *selector arguments*. These arguments are specified inside a comma-separated list within square brackets (`[]`) where each argument has a name and value (e.g. `@e[argument1=value,argument2=otherValue]`, which selects all entities that meet **both** criteria specified by `argument1` and `argument2`). One target selector is `type`, which allows you to filter for specific mobs.

We'll go more into target selector arguments in the next chapters.

### Coordinates

A coordinate describes a position inside of a Minecraft world. The coordinate datatype can describe both an absolute position (i.e a specific point in the world) *as well as* a position **relative** to where the command is being run. When typing commands in chat, the command is run at your position.

>[!TIP]
>
> Use the F3 menu to see at what position you are located in the world; it will be under the `XYZ` field.

#### Format

A coordinate is formatted using three numbers, which correspond to the X, Y, and Z parts of the coordinate respectively; these three numbers are **not** separated by commas. 

As stated earlier, each number can either refer to an absolute (specific) coordinate (e.g. `10 0 -20`), using a decimal/integer, or be *relative* to where the command is run, using a tilde (`~`); for example, the coordinate `~ ~ ~` represents the exact location where the command is being run, no matter where that spot could be.

> [!NOTE]
>
> Sepcifying an integer for the X or Z coordinates (1st and 3rd numbers) automatically centers the coordinate to the center of the corresponding block (e.g. `10 5 -20` would be center-corrected to `10.5 5 -19.5`). This doesn't apply to decimal coordinates, so `10.0, 5, -19.5` won't center-correct the position. The Y coordinate (2nd number) is not affected by center-correction.

You can also mix absolute and relative coordinates (e.g. `10 ~ -20`; where X and Z are specified exactly, but Y is where yours is), and apply an offset to a relative coordinate (e.g. the coordinate `~ ~2.5 ~` is 2.5 blocks upwards from where you are standing)

There is third type of coordinates that's *not compatible* with absolute or relative coordinates, but that won't be learned until the later parts.

### Rotation

A rotation specifies what direction an entity is looking, and is what the `[<rotation>]` argument refers to, and is comprised of 2 numbers: the *yaw* (horizontal rotation) and *pitch* (vertical rotation) respectively, these numbers specify **degrees** instead of radians.

The yaw can range from -180° to +180°; A higher value can be specified, but will wrap back to the stated range, so it's not recommended most of the time. 

>[!NOTE]
>
>For the yaw, 0° points south, 90° points west, 180°/-180° point north, and -90° points east.

The pitch can be a value between -90° (completely upwards) and +90° (completely downwards); very confusing, I know. If the value is outside the range, it will be set either to -90° if less than -90, or to 90° if greater than 90.

Likewise with coordinates, you can use relative rotations (e.g. `~ ~` is your rotation, `~ ~-10` makes you look upward by 10 degrees)

### Usage Within Commands

Now, back to the `tp` command. Here are some examples for you to try, with their corresponding action if you were to run them in the chat:
- `/tp 12 34 56` - teleports you to an arbitrary location;
- `/tp @a @s` - teleports all players to your position;
- `/tp @a ~10 ~ ~` - teleports all players to your coordinates, offset by 10 blocks eastward;
- `/tp ~ 320 ~` - teleports you to the build limit, without changing your horizontal coordinates;
- `/tp @s 230.23 20 168.95 90 0` - teleports you to an arbitrary position while making you look west, without looking up nor down (i.e completely forwards);
- `/tp @e[type=minecraft:cow] ~ ~5 ~` - teleports all cows 5 blocks above you. This examples serves as your first look into the `type` selector argument.

> [!TIP]
>
> If you don't know how to read coordinates and rotation, see (insert chapter 0 here)[]
<!-- Chapter 0 is an optional chapter explaining important mechanics of Minecraft relating to commands, such as the F3/debug menu. -->

### Summary

In this chapter, you have learned: 
- Your second command: `tp`;
  - By extension, you learned how to read more complex syntax;
- How to selected entities on a basic scale;
- How to form coordinates and rotation - both absolute and relative; and
- Some ways to use the `tp` command, as well as a quick look into the `type` selector argument.

The next chapter will continue with even more commands and argument datatypes.