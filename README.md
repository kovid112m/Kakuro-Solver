# Kakuro Puzzle

Kakuro, also known as Cross Sums, is a popular number puzzle game that combines elements of crosswords and Sudoku. 
It originated in Japan and has gained popularity worldwide. The first appearance of Kakuro puzzles in Japanese puzzle magazines can be traced back to the 1980s.

Below is shown a complex Kakuro Puzzle with 13x13 grid.

![Logo](https://github.com/kovid112m/Kakuro-Solver/blob/main/Kakuro%20Images/Kakuro%20Puzzle.png)

***

# Rules of the game

Kakuro is played on a grid, usually a blank grid of squares, with some cells containing numbers. The objective is to fill in the empty cells with digits from 1 to 9, following specific rules:
  1.	Each row and column must contain each of the digits 1 through 9 with no repetition.
  2.	The numbers in each "region" (represented by empty white cells in the grid in Grid 1.1) must add up to the given clue (gray cells) for that region.
  3.	A number cannot be repeated within the region given for the same clue.

***

# Methodology

We will solve the Kakuro Puzzle with the help of gurobi optimizer. To use the optimizer, we will have to define the objective functions and the constraints.

## Objective
  #### Minimize 0

There is no specific objective in this puzzle that we want to solve using the feasible solution. 
Hence, we can set to minimizing/maximizing a constant - Minimize 0 in our case.

## Constraints

  1.	#### Every cell should contain exactly one digit.
  ![Constraint 1](https://github.com/kovid112m/Kakuro-Solver/blob/main/Kakuro%20Images/Constraint%201.png)


  2.	#### No digits should repeat in every row across the clue.
  ![Constraint 2](https://github.com/kovid112m/Kakuro-Solver/blob/main/Kakuro%20Images/Constraint%202.png)

  3.	#### No digits should repeat in every column down the clue.
  ![Constraint 3](https://github.com/kovid112m/Kakuro-Solver/blob/main/Kakuro%20Images/Constraint%203.png)

  4.	#### Sum of the digits in every row clue should be equal to the clue.
  ![Constraint 4](https://github.com/kovid112m/Kakuro-Solver/blob/main/Kakuro%20Images/Constraint%204.png)

  5.	#### Sum of the digits in every column clue should be equal to the clue.
  ![Constraint 5](https://github.com/kovid112m/Kakuro-Solver/blob/main/Kakuro%20Images/Constraint%205.png)

***

## Result & Conclusion

The application of Integer Programming (IP) to solve Kakuro puzzles has yielded promising results, showcasing the efficacy of this mathematical optimization technique in finding optimal solutions. The IP model successfully determined a set of integer values for each cell in the Kakuro Grids 4 and 5, satisfying the specified constraints and producing a solution that adheres to the rules of the game.

The solved Kakuro puzzle demonstrates the versatility of Integer Programming in handling complex logical constraints inherent in the game. Using the same IP model developed, we can find optimal solutions to any type of Kakuro puzzle of varying complexities.

![Solved Kakuro Puzzle](https://github.com/kovid112m/Kakuro-Solver/blob/main/Kakuro%20Images/Solved%20Puzzle.png)
