# readme

This code is a simulation of a system of agents, called "macpans," that move around a grid looking for food. The macpans are of three types: helpful, ungrateful, and tit-for-tat. The simulation also includes the placement of canteens and the possibility of a "ghost attack" that decreases the macpans' food levels.

The Macpan class has the following attributes:

food: the amount of food the macpan has

type: the type of macpan (helpful, ungrateful, or tit-for-tat)

x: the x-coordinate of the macpan on the grid

y: the y-coordinate of the macpan on the grid

directional_food_prob: a list of four probabilities representing the likelihood of finding food in each direction (up, right, down, left)

previous_food_avg: the average amount of food the macpan has encountered in its previous locations

history: only for tit-for-tat macpans, it keeps track of whether the macpan has been helped by another macpan


The Grid class has the following attributes:

GRID_SIZE: the size of the grid

NUM_CANTEENS: the number of canteens placed on the grid

NUM_DAYS: the number of days the simulation runs for

GHOST_ATTACK: the amount of food lost by a macpan in a ghost attack

CANTEEN_FOOD: the amount of food added to a macpan's food level when it eats at a canteen

REPRO_THRESHOLD: the food level a macpan needs to reproduce

EXCESS_THRESHOLD: the food level at which a macpan stops moving to conserve energy

MAX_POPULATION: the maximum number of macpans allowed on the grid

grid_canteen: a matrix representing the placement of canteens on the grid

grid_object: a matrix of lists representing the location of macpans on the grid

num_helpful_macpan: the number of helpful macpans on the grid

num_ungrateful_macpan: the number of ungrateful macpans on the grid

num_tit_for_tat_macpan: the number of tit-for-tat macpans on the grid

num_canteens_placed: the number of canteens actually placed on the grid

num_macpan: the total number of macpans on the grid

num_macpan_died: the number of macpans that died during the simulation

num_macpan_reproduced: the number of macpans that reproduced during the simulation


The Grid class has the following methods:

place_macpan: places a macpan on the grid at a random location

place_canteens: places canteens on the grid at random locations

ghost_attack: simulates a ghost attack, which reduces the food level of macpans and can lead to their death
movement_intel_grid: updates the macpan's location and its directional food probabilities based on the average food levels of other macpans in its new location. This method also handles the movement of the macpan and updates its previous food average.
