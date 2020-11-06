# The-Game-of-Life
Conway's Game of Life using Matplotlib

The Game of Life is a cellular automata simulation that runs based on the following rules:

    1. Any live cell with fewer than two live neighbors dies, as if by underpopulation.
    2. Any live cell with two or three live neighbors lives on to the next generation.
    3. Any live cell with more than three live neighbors dies, as if by overpopulation.
    4. Any dead cell with exactly three live neighbors becomes a live cell, as if by reproduction.

My process was centered around a numpy array with 0's representing the dead state while 1's represent the alive state. Python arrays allow for going backwards with negative numbers, so this made determining each cell's neighbors only require a general algorithm. Being able to determine the cell's neighbors allowed
