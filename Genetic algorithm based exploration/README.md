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
