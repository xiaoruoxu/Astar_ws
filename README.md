# Introduction
The A* algorithm, or A-star algorithm, is a widely used heuristic search algorithm for graph search and pathfinding. It is a general-purpose algorithm used to find the shortest or optimal path from a starting node to a target node. A* algorithm combines the principles of Dijkstra's algorithm for unweighted graph search and the greedy algorithm for heuristic search to improve search efficiency.  
Here's how the A* algorithm works:

**Initialization**  
Place the starting node in an open list with a cost of 0. Create an empty closed list to keep track of processed nodes.

**Loop**  
Repeat the following steps until a termination condition is met:  
a. Select the node with the lowest cost (combining the actual path cost and the estimated future cost) from the open list as the current node.   
b. Move the current node from the open list to the closed list to mark it as processed.   
c. For each neighbor of the current node:
-   If the neighbor is not in the closed list and is not in the open list or has a lower path cost, calculate the cost (combining actual and estimated cost) and add it to the open list.
-   If the neighbor is already in the open list, check if the new path to it has a lower cost. If so, update the cost and set the current node as the parent.

**Termination Condition**  
The algorithm terminates when the target node is found, or when the open list becomes empty, indicating that there is no valid path to the target.
    
**Path Backtracking**  
If the target node is found, backtrack from the target node to the start node by following the parent nodes, forming the optimal path.  

The key to A* algorithm lies in its heuristic function, which is used to estimate the cost from the current node to the target node. This heuristic function must satisfy certain conditions, with the most crucial being that it should not be overly optimistic and should not underestimate the actual cost; otherwise, A* algorithm may not find the optimal path. One commonly used heuristic function is the Manhattan distance, suitable for grid-based pathfinding problems.  

A* algorithm is widely applied in pathfinding, game development, robot navigation, and various other fields because it efficiently finds the best path and can adapt to different types of problems by using different heuristic functions.

# Usage
The code demonstrates two path planning algorithms, A* and JPS, along with a comparison of their planning times. Here are the steps for running the code.

**1、Download Code**
```
git clone https://github.com/xiaoruoxu/Astar_ws
```
**2、Compile**
```
cd ~/Astar_ws
catkin_make
source devel/setup.bash
```
**3、Run The Code**
```
roslaunch grid_path_searcher demo.launch
```
