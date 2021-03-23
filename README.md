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

Genetic algorithm based exploration: <br>
Lab3: The drone has a battery. This means that it can travel only a certain amount of positions (INDIVIDUAL_SIZE). Also other parameters can be set:
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

Depth first search based exploration: The drone explores the map in a depth first search manner. The speed can be adjusted using left and right arrow.

![lab1-1](https://user-images.githubusercontent.com/46956225/111899220-d23b5100-8a33-11eb-8988-1055ed268033.png)

![lab1-2](https://user-images.githubusercontent.com/46956225/111899219-d1a2ba80-8a33-11eb-93ef-573864843c9a.png)


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


