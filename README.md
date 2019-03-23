# fitz
A tile based multiplayer console game, programmed in C99. Comes with two automated player so it's alright if you don't have friends!

## Compile Instruction
Compile `fitz.c` with gcc. Alternatively, `make` with the provided makefile. 

## Usage Instruction
`Usage: fitz tilefile [p1type p2type [height width | filename]]`

## The Game
The game begins with an empty board, displayed like this (this is an example of a 4x5 board):
```
.....
.....
.....
.....
```

The two players in the game will take turns getting a tile from a file and placing it onto the board. Tiles can be rotated clockwise (in multiples of 90 degrees) before being placed. For example, a tile shaped like this:
```
****
```
could be placed in any of the following ways (as well as others):
```
*....   .....   ....*   .....
*....   .....   ....*   .....
*....   ****.   ....*   .....
*....   .....   ....*   .****
```
The first player will indicate their tiles with * and the second player will use #. A tile can not be placed where it will overlap with existing tiles on the board..The game ends when a player can not place their next tile. That player loses. For example, the * player needing to place
```
**
**
```
on a board that looks like:
```
#####
.**##
**..#
.****
```
would lose the game. The tiles must be used in the order they appear in the file. If you run out of tiles, start again at the beginning of the file.
