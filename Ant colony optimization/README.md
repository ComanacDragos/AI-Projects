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

