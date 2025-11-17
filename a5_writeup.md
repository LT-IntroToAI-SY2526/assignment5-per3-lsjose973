# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. What are some things that you learned through this assignment? Think about the concepts of backtracking, constraint satisfaction, and search algorithms. Were there any particular challenges you faced while implementing the Board class methods or the DFS/BFS functions? How did you overcome them?

Some things I learned through this assignment were how to traverse through 3d arrays in the context of a sudoku board, as well as how backtracking and constraint satisfaction work as code and not just as concepts. When I was writing the update function, I really saw how constraint satisfaction works, as we had to remove the number we just placed from every other cell in the same row, column, or subgrid of that cell. I saw backtracking when we were writing the DFS functions, when we pop the contradicting boards off of the stack. I also understood how search algorithms like DFS and BFS work, and the difference between going "Depth" and "Breadth" when searching for a solution. 


2. How can you apply what you learned in this assignment to future programs or projects? Consider other types of problems that involve searching through possibilities, making decisions, and backtracking when those decisions don't work out. Can you think of real-world scenarios where DFS or BFS might be useful? What about other constraint satisfaction problems?

This assignment taughe me how many problems in programming consist of the same principles of searching through possibilities, following constraints, and backtracking when contradictions occur. Other types of problems that involve searching throuh possibilities, making decisions, and backtracking could include trying to find the exit to a maze. DFS and BFS would be useful because it would track the different possible paths you can take and find you the correct one. The idea of constraint satisfaction was useful to learn about since it applies to other problems where you need to satisfy multiple rules at once.

3. Explain how the Stack and Queue classes work and why they are important for DFS and BFS algorithms. Describe the difference between LIFO (Last In First Out) and FIFO (First In First Out) data structures. How does using a Stack versus a Queue change the way the search algorithm explores possible solutions? Why is one data structure better suited for depth-first search and the other for breadth-first search?

The stack class follows LIFO, which means that the most recently added item is the first one that will be taken out. For example, when you're eating pancakes, you place the last pancake on top but you eat that one first. A queue follows FIFO, which means that the first item to be added will be the first one to be taken out. For example, if a line of peope are waiting at a restauraunt, the people who got there first will be the first ones let in. The stack class is important for the DFS algorithm because DFS always wants to search the most recent decision first. When it pushes a new state onto the stack, it goes deeper, and if it finds a contradiction, it goes back to the most recent one it just pushed. The LIFO nature of the stack class works for depth-first searching because you only need to store the current path and backtracking points. The queue clsas is important for the BFS algorithm because BFS wants to search the paths by each level. It processes the boards in the order they were pushed, checking each new state and only throwing it away when a contradiction is found. The FIFO nature of the queue class works for breadth-first searching because it makes the algorithm expand the boards that were pushed at the start first, and the boards pushed later after that. It explores all the boards at one level, because they were the first ones pushed in, and then the next level, because those were the next ones pushed.