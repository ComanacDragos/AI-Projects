# AI-Projects

Collection of AI projects implemented for the Artificial Intelligence course
The implementation is a refactorization of the given starting code consisting of the pictures and the map in pygame. The refactorization consists of layered architecture and scalable map. For each project I implemented the algorithms that move the drone across the map. Also the settings of the algorithms can be set from the settings file.

Lab1: Depth first search based exploration <br>
Lab2: Greedy, A*, Tabu search, simulated annealing path finding <br>
Lab3: Genetic algorithm based exploration

Lab1: The drone explores the map in a depth first search manner. The speed can be adjusted using left and right arrow.

![lab1-1](https://user-images.githubusercontent.com/46956225/111899220-d23b5100-8a33-11eb-8988-1055ed268033.png)

![lab1-2](https://user-images.githubusercontent.com/46956225/111899219-d1a2ba80-8a33-11eb-93ef-573864843c9a.png)


Lab2: The drone finds the path between 2 points on the map. The position of the drone can be set with right-click and the destination position can be set with left click. Greedy and A* can be shown by pressing G, Tabu by pressing T ( tabu search doesn't always find a path) and simulated annealing by pressing S (C can be pressed to find another path for simulated annealing). <br>

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
