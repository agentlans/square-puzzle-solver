# square-puzzle-solver
Solves the sliding 8-puzzle and 15-puzzle

## Introduction
Sliding puzzles are played on a board with numbered tiles in a rectangular array.
One of the spaces is empty and the tiles next to that space can slide into that space.
The object of the game is to slide the tiles to put their numbers in order.

The 8-puzzle and 15-puzzle refer to the 3 x 3 and 4 x 4 puzzles, respectively.

## Install
Requires:
- Common Lisp installation
- Roswell build system
- `alexandria` and `cl-str` packages from Quicklisp

(Optional) You can make an executable by running `ros build square-puzzle.ros`.

## Use

To generate and solve a n x n square puzzle, run `./square-puzzle.ros n`.
To solve a puzzle from a given arrangement, run `./square-puzzle.ros puzzle.txt` where `puzzle.txt` is a text file containing your starting position.

Notes:
- puzzles larger than 4 x 4 may take a very long time
- this program may not give the optimal solution (fewest number of moves)
- not every puzzle position can be solved. In that case, the program won't finish.

**Example input file:**

0 represents the empty space.
```
4,7,8,1 
13,6,2,3 
5,10,0,11 
12,14,9,15
```

**Example output:**

Output shows the puzzle after each move in the solving process.
_ represents the empty space.

```
 4  7  8  1 
13  6  2  3 
 5 10  _ 11 
12 14  9 15 

 4  7  8  1 
13  6  2  3 
 5  _ 10 11 
12 14  9 15 

 4  7  8  1 
13  6  2  3 
 _  5 10 11 
12 14  9 15 

...[more moves omitted]

 4  1  2  3 
 _  5  6  7 
 8  9 10 11 
12 13 14 15 

 _  1  2  3 
 4  5  6  7 
 8  9 10 11 
12 13 14 15 
```

## Author, License

Copyright (C) 2020  Alan Tseng

GNU General Public License v3
