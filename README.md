# Advanced Search Algorithms Implementation

Files are separated into two folders

## Instruction

Run the code. Navigating under each of the two folders, and run

`python main.py`


## D*


1. The **run** function is the main function of D* algorithm, which includes two main steps. The first step is to search from goal to start in the static map. The second step is to move from start to goal. If any change detected in the second step, the cost is updated and a new path is replanned.
2. The **process_state** function that pops node from the open list, and process the node and its neighbors based on the state. 
3. The **prepare_repair** function that senses the neighbors of the given node and locate the new obstacle nodes for cost modification.
4. The **modify_cost** function that modifies the cost from the obstacle node and its neighbor, and put them in the Open list for future search.
5. The **repair_replan** that replans a path from the current node to the goal

For more details, please go through the lecture and the original paper [Optimal and Efficient Path Planning for Partially-Known Environments](http://web.mit.edu/16.412j/www/html/papers/original_dstar_icra94.pdf). Read the description of the functions and follow the steps.

## Informed RRT*

Most of the code structure is the same as the RRT*'s with a few additions,
1. The first part is within the **main** function of informed RRT, the c_best - best length of the path when a path is found. 
2. The second part is within the **sample** function. Different sampling functions are used based on the c_best value. 
3. The last part is the implementation of the ellipsoid sampling **get_new_point_in_ellipsoid**, so that when a path is found, the samples will be cast within an ellipsoid area for faster convergence.

For more details, please go through the lecture and the original paper [Informed RRT*: Optimal Sampling-based Path Planning Focused via Direct Sampling of an Admissible Ellipsoidal Heuristic](https://arxiv.org/pdf/1404.2334.pdf). Read the description of the functions and follow the steps.

