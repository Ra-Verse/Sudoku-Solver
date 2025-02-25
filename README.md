# Sudoku Solver (C++)

This repository contains a Sudoku solver implemented in C++, utilizing a backtracking algorithm.

## Description

This program solves Sudoku puzzles by implementing a backtracking algorithm. It takes a 9x9 Sudoku grid as input, where empty cells are represented by zeros, and attempts to find a valid solution.

**Key Features:**

* **Backtracking Algorithm:** Employs a recursive backtracking approach to explore possible solutions.
* **C++ Implementation:** Written in standard C++ for efficiency and portability.
* **Input Validation:** Includes input validation to ensure the Sudoku puzzle is entered correctly.
* **Formatted Output:** Presents the solved Sudoku grid with clear formatting.
* **User-Friendly Input:** Prompts the user to enter the Sudoku puzzle row by row.

**How it Works:**

1.  **Input Acquisition:** The `get_input` function prompts the user to enter the Sudoku puzzle, validating each row to ensure it contains 9 numbers between 0 and 9.
2.  **Backtracking Solver:** The `solve` function uses a recursive backtracking algorithm:
    * It finds an empty cell.
    * It attempts to place numbers 1 to 9 in the cell.
    * The `is_valid` function checks if the placement is valid according to Sudoku rules.
    * If the placement is valid, it recursively calls `solve` to continue solving.
    * If a placement leads to a dead end, it backtracks by resetting the cell to 0.
3.  **Output Display:** If a solution is found, the solved grid is printed in a formatted manner. If no solution exists, a message is displayed.

**Code Structure:**

* `main()`: Handles program execution, input, solution, and output.
* `is_valid()`: Checks if a number can be placed in a given cell according to Sudoku rules.
* `solve()`: Implements the backtracking algorithm.
* `get_input()`: Gets and validates the Sudoku puzzle input from the user.

**Usage:**

1.  Compile the C++ code.
2.  Run the executable.
3.  Enter the Sudoku puzzle row by row, using spaces to separate numbers and 0 for empty cells.
4.  The program will output the solved Sudoku grid or indicate that no solution exists.

**Example Input:**

<pre>
0 3 0 0 5 0 0 4 0
0 0 8 0 1 0 5 0 0
4 0 0 8 0 6 0 0 1
0 0 5 0 0 0 9 0 0
7 0 0 0 0 0 0 0 8
0 0 9 0 0 0 2 0 0
2 0 0 5 0 9 0 0 7
0 0 1 0 7 0 4 0 0
0 8 0 0 4 0 0 1 0
</pre>

**Example Output:**

<pre>
9  3  2  |  7  5  1  |  8  4  6
6  7  8  |  4  1  2  |  5  9  3
4  5  7  |  8  9  6  |  3  2  1
---------+-----------+---------
8  2  5  |  1  3  4  |  9  6  7
7  1  6  |  9  2  5  |  3  5  8
3  4  9  |  6  8  7  |  2  1  5
---------+-----------+---------
2  6  4  |  5  8  9  |  1  3  7
5  9  1  |  2  7  3  |  4  8  6
1  8  3  |  6  4  8  |  7  1  9
</pre>
