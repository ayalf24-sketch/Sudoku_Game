# Sudoku_Game
My CS112 Final Project


**Sudoku Solver (Java)**

A Java program that reads a Sudoku puzzle from a file, displays it, and solves it using recursive backtracking. This project demonstrates constraint checking, recursion, and efficient Sudoku solving.

**Features**

Sudoku Board Representation:

9x9 grid implemented with a 2D array.

Tracks fixed values and dynamically placed values.

Efficiently checks rows, columns, and 3x3 subgrids for validity.

Input/Output:

Reads puzzle configurations from a text file.

Displays the puzzle in a clean, readable console format.

Shows row separators to make 3x3 subgrids visually distinct.

**Solver:**

Uses recursive backtracking to find solutions.

Ensures safe placement by checking rows, columns, and subgrids.

Can report if no solution exists.

**Implementation Details**

Data Structures:

grid[9][9] — stores current puzzle values.

valIsFixed[9][9] — tracks initially fixed numbers.

subgridHasVal[3][3][10], ValRow[9][10], ValCol[9][10] — boolean arrays for fast constraint checking.

**Key Methods:**

placeVal(val, row, col) / removeVal(val, row, col) — place or remove a number from the grid.

checkifSafe(row, col, val) — returns true if a value can be placed in a cell safely.

solveRB(n) — recursive backtracking method that attempts to solve the puzzle.

solve() — public wrapper that starts the backtracking process.

printGrid() — prints the current state of the puzzle in a formatted grid.

**File Input:**
Reads a file containing 9x9 numbers (0 for empty cells).

Handles file I/O exceptions gracefully.

**Notes**

The solver is fully automated; no user input is required beyond the puzzle file.

Uses backtracking efficiently by skipping fixed cells and validating constraints before each placement.
