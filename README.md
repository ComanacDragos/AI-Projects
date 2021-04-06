# AI-Projects

Collection of AI projects implemented for the Artificial Intelligence course
The implementation is a refactorization of the given starting code consisting of the pictures and the map in pygame. The refactorization consists of layered architecture and scalable map. For each project I implemented the algorithms that move the drone across the map. Also the settings of the algorithms can be set from the settings file.

Genetic algorithm based exploration <br>
Depth first search based exploration <br>
Greedy, A*, Tabu search, simulated annealing path finding <br>

Requirements:
- pygame
- numpy
- matplotlib

Ant colony optimization: <br>
The drone has a battery. This means that it can travel only a certain amount of positions (ANT_SIZE). <br>A number of sensors are placed on the map. Each sensor can be charged with a maximum amount of energy. The task of the drone is to charge as many sensors as possible with as much energy as possible with the available energy in the battery. Each step is equivalent with 1 energy. The drone can charge a sensor with energy from 0 to SENSOR_STRENGTH.<br><br>

The drone togheter with the sensors are considered as a graph. First ant colony optimization is applied to find out the paths between each pair of vertices (an edge is the path and it's cost is the length of the path). Then the problem can be regarded similar to the travelling salesman problem. Ant colony optimisation is used to find the shortest path between all vertices and a random energy is used on each sensor. The ant that left the most energy for the sensors with as little energy as possible (minimize length of the path and maximize the energy for the sensors) is considered the best.

<br>

Press d to show/hide the energy left to the sensors (with red are displayed the squares that could have been charged and with yellow those that are charged, and with green is diasplayed the path).
<br>
Press r to reset the drone and sensors positions.
Right click a square to place the drone in the given square and start the algorithm.

<br>
Also other parameters can be set:
<ul>
  <li>ANT_SIZE: size of the battery</li>
  <li>EPOCHS: number of epochs</li>
  <li>NO_ANTS: number of ants</li>
  <li>ALPHA: how much the cost of a edge matters in choosing next move</li>
  <li>BETA: how much the pheromone on a edge matters in choosing next move</li>
  <li>DECAY: the rate at which the pheromones decay after one epoch</li>
  <li>Q: initial pheromones on each edge</li>
  <li>Q0: probability that a move is chosen as the maximum of the product of cost and pheromones, otherwise choose next move besed on a roulette</li>
  <li>SENSORS: number of sensors</li>
  <li>SENSOR_STRENGTH: maximum number of squares a sensor can see in a direction</li>
  <li>EARLY_STOP: number of epochs after which the algorithm stops if there are no improvements</li>
</ul>

![ACO](https://user-images.githubusercontent.com/46956225/113742368-3ab05080-970b-11eb-8a33-e09c7b14c8a5.png)

![ACO2](https://user-images.githubusercontent.com/46956225/113742765-9da1e780-970b-11eb-8d64-f8ad0dde1f0a.png)

Genetic algorithm based exploration: <br>
The drone has a battery. This means that it can travel only a certain amount of positions (INDIVIDUAL_SIZE). Also other parameters can be set:
<ul>
  <li>POPULATION_SIZE: size of the populations</li>
  <li>GENERATIONS: number of generations</li>
  <li>MUTATE_PROB: probablity that a mutation occurs in an individual</li>
  <li>CROSSOVER_PROB: probability that a crossover occurs between 2 individuals</li>
  <li>ERROR_FACTOR: the factor by which the error it's multiplied in the fitness function</li>
  <li>GENE_STRENGTH: the strength of a gene (the number of times it appears consecutively in a chromosome</li>
  <li>FITNESS_FUNCTION: the fithess function (the uniquePositionsFitness function for as many detected positions as possible, circularFitness brings the drone to the original position </li>
  <li>ITERATION_STRATEGY: steady state / generational</li>
  <li>STEADY_STATE_NO_OFFSPRINGS: the number of possible offsprings generated in steady state strategy</li>
</ul>

A gene is represented by a basic direction ((1, 0), (0, 1), (-1, 0), (0, -1)) and a strength (essentially a gene is a 2 dimensional vector) which is a random number between 1 and GENE_STRENGTH. An individual is composed of multiple basic directions, each basic direction appearing based on it's strength (for example if the strength is 3 then the basic direction will appear 3 times in the individual, consecutive).

The mutation consists of changing a random gene in an another random gene (only one basic direction is changed into another basic direction).

The crossover consists of splitting the source and destination at a random index, the the offsping takes the left part from source and right part from destination.

![lab3-1](https://user-images.githubusercontent.com/46956225/111905706-b8ab0100-8a55-11eb-8924-c6853e3cc559.png)

![lab3-2](https://user-images.githubusercontent.com/46956225/111905710-b9439780-8a55-11eb-8417-41f2ed75b4c8.png)

![lab3-3](https://user-images.githubusercontent.com/46956225/111905711-b9439780-8a55-11eb-81cd-b8cc853b8033.png)

![lab3-4](https://user-images.githubusercontent.com/46956225/111905705-b8126a80-8a55-11eb-8a3b-a7b2c0d11694.png)

A path can be loaded with CTRL + L and can be saved with CTRL + S. With rightclick the drone can be moved to a new direction and the algorithm begins.

Greedy, A*, Tabu search, simulated annealing path finding: The drone finds the path between 2 points on the map. The position of the drone can be set with right-click and the destination position can be set with left click. Greedy and A* can be shown by pressing G, Tabu by pressing T ( tabu search doesn't always find a path) and simulated annealing by pressing S (C can be pressed to find another path for simulated annealing). <br>

For simulated annealing the keep probability can be set (the probability that a bad solution is kept) and the early stop can be set (the number of iteration 

Color coding: 
Red - Greedy <br>
Yellow - A* <br>
Green - Common for Greedy and A* <br>
Purple - Tabu search <br>
Blue - Simulated annealing <br>

![lab2-1](https://user-images.githubusercontent.com/46956225/111899377-02cfba80-8a35-11eb-8c45-5f3eb3cb992e.png)

![lab2-2](https://user-images.githubusercontent.com/46956225/111899380-0400e780-8a35-11eb-91cb-a6fbf1d74970.png)

![lab2-3](https://user-images.githubusercontent.com/46956225/111899379-03685100-8a35-11eb-8175-1fc98ed7a351.png)

<br>
Depth first search based exploration: The drone explores the map in a depth first search manner. The speed can be adjusted using left and right arrow.

![lab1-1](https://user-images.githubusercontent.com/46956225/111899220-d23b5100-8a33-11eb-8988-1055ed268033.png)

![lab1-2](https://user-images.githubusercontent.com/46956225/111899219-d1a2ba80-8a33-11eb-93ef-573864843c9a.png)


