# Problem statement: Develop python codes in modular fashion to perform the following functions:
Read data from the file test_data.txt. Achieve a good floorplan using Simulated Annealing algorithm. Using matplotlib or any other suitable library plot the given objects in Jupyter IDE.

## Given data:
1) Number of blocks
2) An adjacency matrix representing number of wires between block i and block j. Where block i is represented in row i and block j is represented in column j of the matrix. 
3) Data of the blocks in the format {block_ID block_width block_height} 
4) Normalized Polish Expression of the initial floor plan.

## Constraints: 
Assume all blocks are hard blocks with fixed dimensions, orientation of the blocks can not be changed and only one shape is available.

### Cost is defined as weighted sum of area 'A' of the layout and overall wiring length 'W'. The cost C is given by C=0.75A+0.25W.
(Area) A of this layout is the area of smallest possible rectangle covering all the blocks (Wiring length) W = Summation of (cij · dij) over all i and j where cij is equal to the number of connections between blocks i and j, provided in adjacency matrix and dij is the center-to-center distance between basic rectangles i and j.

Compute the cost of initial floor plan for the initial SCORE in simulated annealing. 
Goal is to minimize this cost by applying 3 moves iteratively. 

## Output:
At the end of every iteration:
Print the overall area, wirelength, cost, Normalized polish expression of floor plan and Plot the floorplan. 
Finally plot the horizontal and vertical polar graphs of the layout. 

Test data: (Found in the test_data.txt)
n=7
Adjacency matrix regarding the number of wires between the blocks
{{0 1 2 1 0 1 1}  
{1 0 1 2 1 2 1}  
{2 1 0 1 1 1 2}  
{1 2 1 0 1 1 1}  
{0 1 1 1 0 1 1}  
{1 2 1 1 1 0 1}  
{1 1 2 1 1 1 0}}  
Data regarding the Blocks in the format {block_ID block_width block_height} 
{1 10 10}  
{2 10 15}  
{3 10 5}  
{4 5 10}  
{5 5 5}  
{6 15 10}  
{7 5 5}  

Polish Expression of the Initial Floorplan: 1 2 V 3 H 4 5 6 V H 7 V H

