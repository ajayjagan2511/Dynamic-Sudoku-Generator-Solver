# Dynamic-Sudoku-Generator-Solver
A C++ Program that can generate new puzzles and solve incomplete puzzles in Sudoku. Can do so for upto 16x16 puzzles.

A project that is implemented in c++ whose purpose is twofold. 

First is to generate a 4*4, 9*9 or 16*16 matrix that follows the rules of sudoku game.
ie. in a N*N matrix each position can only be occupied by an element within 1 to N and such that, that element does not occur again in its corresponding row, column or box.
The naive implementation time complexity of N^(N*N) is reduced to (n-sqrt(n))^(n-sqrt(n)*n-sqrt(n)) (all worst case) by filling the diagonal boxes without any restrictions.
Non-diagonal matrices are filled recurcively.This enables 16*16 matrix generation by reducing time complexity. 
Now K random numbers are removed, such that a matrix that the user can solve is generated.

Second is to complete an incomplete sudoku matrix provided by the user.
First, it is checked if the entered matrix is valid.
If so, then it is completed.
This is done by recursively traversing each index in order, placing an valid element in the space and checking if this will lead to a valid matrix.
If the matrix is not valid, then the next valid element is put in the space and checked.
The first valid matrix obtained is returned.

Tech stack involved- c++17

Concepts Involved-
OOPs- classes and objects, polymorphism (constructor overloading)
Recursion
Backtracking
Data Structures-Vectors
STL functions-random_shuffling of a vector
srand(time(NULL)- for time varying randomization of random_shuffling and rand() 
