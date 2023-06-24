# Sudoku Solver and Generator

This program solves user-inputted Sudoku puzzles and generates random unsolved Sudoku puzzles for the user to test out. The main compenent is a backtracking algorithm to efficiently solve any Sudoku grid.

## How to Use

1. Clone the repository or download the `sudoku.cpp` file.
2. Compile the code using a C++ compiler.
3. Run the executable file.

## Program Overview

The program provides a menu with the following options:

1. Generate New Sudoku: Generates a new random unsolved Sudoku puzzle and displays it.
2. Solve Sudoku: Solves the Sudoku puzzle if it is solvable and displays the solution.
3. Input Custom Sudoku: Allows the user to input a custom Sudoku puzzle and displays it.
4. Quit: Exits the program.

## Functionality

### `solvePuzzle` Function

This function solves the Sudoku puzzle recursively. It finds every empty cell in the given Sudoku and replaces it with a valid number according to the rules of Sudoku. Backtracking occurs when an earlier assumption of a valid number was incorrect. Recursive calls continue until a solvable solution is found.

### `isValid` Function

This function checks if a given number (`n`) matches a number in the same column, row, or subgrid of the Sudoku puzzle. It returns `true` if the number is valid and `false` otherwise.

### `displayPuzzle` Function

This function displays the Sudoku puzzle in a separated manner. It uses horizontal and vertical dashes to divide the Sudoku into subgrids for better readability.

### `generateSudoku` Function

This function generates a random unsolved Sudoku puzzle. It creates a new Sudoku puzzle by first solving a completely filled puzzle and then removing 40 cells to create some difficulty. The generated puzzle is stored in the provided 2D vector `puzzle`.

## Author

This program was written by Yasna Rezvani on June 23, 2023.

## Note

This program assumes a 9x9 Sudoku grid. Ensure that the input adheres to the correct format to avoid errors.
