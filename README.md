Light Up Solver
---------------------------

# Introduction

In this project, we wrote a Python program to solve the Light Up
puzzle using a SAT solver.
In the puzzle Light Up ([http://www.nikoli.co.jp/en/puzzles/akari][akari]), you are presented with a grid with obstacles and numbers.
When lights are placed in empty spaces on the puzzle, they illuminate in each of the four directions on the grid until a wall, obstacle, or number is reached.
The object of the puzzle is to place lights such that each empty space on the grid is illuminated, no two lights can light one another, and for each
number on the grid, exactly that many lights are adjacent to that space.

[akari]:http://www.nikoli.co.jp/en/puzzles/akari.html

Our program should read in a puzzle from a textfile given as a command-line argument, encode this instance as a boolean forumula
in CNF such that satisfying assignments correspond to solutions to the puzzle, and use a SAT solver from the Python-SAT package to
find a satisfying assignment to this formula (or state that none exist).

Five puzzles have been included below (and textfiles for each are included in the starter code on github).
In each puzzle, "`.`" represents an empty space, "`X`" represents an obstacle, and each number "`0`", "`1`", "`2`", "`3`", "`4`" represents
the constraint that exactly that many lights are adjacent in a solution.

**Puzzle 1**
```
..X
.1.
```

**Puzzle 2**
```
....
.1.X
1X..
..2.
```

**Puzzle 3**
```
.0...2
...X..
2X..4.
..1...
....X.
```

**Puzzle 4** [Source][puzzle4]
```
..X...X
.4..1.X
...2...
.X...X.
...X...
X.X..1.
1...1..
```

**Puzzle 5** [Source][puzzle5]
```
X..X.....X
.......X..
.3....0...
..2..X...1
...10X....
....1XX...
X...2..2..
...X....X.
..1.......
0.....1..0
```

[puzzle4]: http://www.nikoli.co.jp/en/puzzles/akari.html 
[puzzle5]: https://en.wikipedia.org/wiki/Light_Up_(puzzle)

Given a puzzle as described above, a correct program will either output that no solution exists, or print a solution with the lights represented as `O`.
For example, given Maze 4 above, a correct program outputs the following.
```
.OX..OX
O4O.1.X
.O.2O..
.X.O.X.
...X..O
X.XO.1.
1O..1O.
```


