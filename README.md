# The-Game-of-Life
Conway's Game of Life using Matplotlib

The Game of Life is a cellular automata simulation that runs based on the following rules:

    1. Any live cell with fewer than two live neighbors dies, as if by underpopulation.
    2. Any live cell with two or three live neighbors lives on to the next generation.
    3. Any live cell with more than three live neighbors dies, as if by overpopulation.
    4. Any dead cell with exactly three live neighbors becomes a live cell, as if by reproduction.

My process was centered around a numpy array with 0's representing the dead state while 1's represent the alive state. Python arrays allow for moving backwards through them with negative numbers, so this made determining each cell's neighbors not require a position dependent algorithm, also thanks to the periodic boundaries. 
Determining a cells neighbor goes as follows: 
         
         prev_i= i-1 # Negative numbers moves to top of numpy
         prev_j = j-1 # negative numbers move to left of numpy
         next_i = (i +1)% self.size # If the i is greater than the array size, moves to first array
         next_j = (j+1) % self.size # If the j is greater than the array size, moves to left side,
         
         neighbor_sum = (cells[prev_i][prev_j] + cells[prev_i][j] + cells[prev_i][next_j] # Sum of all 9 neighbors.
                + cells[i][prev_j] + cells[i][next_j]
                + cells[next_i][prev_j] + cells[next_i][j] + cells[next_i][next_j])
By applying the neighbor sum to the rules of the game, the cell's next state could be determined through each evolution of the simulation.
