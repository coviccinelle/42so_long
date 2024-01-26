
# **So Long** _And Thanks for All the Fish_!

## Table of Contents
1. [Common Instructions](#common-instructions)
2. [Mandatory Part - Program name: so_long](#mandatory-part)
   - [Files to Turn In](#files-to-turn-in)
   - [Arguments](#arguments)
   - [External Functions](#external-functions)
   - [Libraries](#libraries)
   - [Description](#description)
3. [Game](#game)
   - [Player's Goal](#players-goal)
   - [Controls](#controls)
   - [View](#view)
   - [Real-time Requirement](#real-time-requirement)
4. [Graphic Management](#graphic-management)
   - [Window Display](#window-display)
   - [Window Management](#window-management)
   - [Image Usage](#image-usage)
5. [Map](#map)
   - [Map Components](#map-components)
   - [Valid Map Conditions](#valid-map-conditions)
   - [Map Structure](#map-structure)

## Common Instructions
- Written in C.
- Adherence to the Norm for bonus files/functions.
- Functions should not cause unexpected exits (segmentation fault, bus error, etc.).
- Proper freeing of heap allocated memory, no memory leaks.
- Submission of a Makefile for compilation.
- Use of `-Wall`, `-Wextra`, and `-Werror` flags in the Makefile.
- Makefile must contain rules: `$(NAME)`, `all`, `clean`, `fclean`, and `re`.
- Bonus submission includes a separate `_bonus.{c/h}` file.
- If allowed to use libft, copy sources and Makefile to a `libft` folder.

## Mandatory Part

### Files to Turn In
- Makefile, *.h, *.c, maps, textures

### Arguments
- A map in the format *.ber

### External Functions
- `open`, `close`, `read`, `write`, `malloc`, `free`, `perror`, `strerror`, `exit`
- All functions of the math library (-lm compiler option, `man man 3 math`)
- All functions of the MiniLibX
- `ft_printf` and any equivalent YOU coded

### Libraries
- Libft authorized

### Description
Create a basic 2D game where a character escapes after collecting items. Use MiniLibX for graphical display. The program must take a map description file with a .ber extension.

## Game

### Player's Goal
- Collect all items on the map and escape choosing the shortest route.

### Controls
- W, A, S, D keys for character movement.
- Up, down, left, right movement allowed.
- Player cannot move into walls.
- Display current movements in the shell.

### View
- 2D view (top-down or profile).
- Non-real-time gameplay.

## Graphic Management

### Window Display
- Display the image in a window.
- Smooth window management (changing, minimizing, etc.).

### Window Management
- Pressing ESC must close the window and quit cleanly.
- Clicking on the window's cross must close the window and quit cleanly.

### Image Usage
- Use images of the MiniLibX.

## Map

![image](https://github.com/coviccinelle/42so_long/assets/51762886/acd1cd94-6e44-4d1d-8b3a-7b4b2c5dd75d)


### Map Components
- Walls, collectibles, free space.
- Valid characters: 0 (empty), 1 (wall), C (collectible), E (exit), P (player's position).

### Valid Map Conditions
- Must contain 1 exit, at least 1 collectible, and 1 starting position.
- No duplicate exit/start characters.
- Must be rectangular.
- Must be closed/surrounded by walls.

### Map Structure
- Parse any valid map respecting specified rules.
- Handle misconfigurations and errors gracefully.

