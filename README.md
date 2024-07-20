# Task-scheduling-using-cuckoo-search-algorithm
The Cuckoo Search algorithm is a nature-inspired optimization algorithm based on the brood parasitic
behavior of certain cuckoo species. It uses Lévy flights to explore the search space and a fraction
probability to abandon worse solutions, ensuring a good balance between exploration and exploitation. </br>
The steps involved in the Cuckoo Search algorithm for task scheduling are: </br>
1. Initialization: Create an initial population of nests (solutions).
2. Lévy Flights: Generate new solutions (cuckoos) by performing Lévy flights.
3. Fitness Evaluation: Evaluate the fitness of each solution based on the makespan.
4. Fitness Evaluation: Evaluate the fitness of each solution based on the makespan.
5. Abandonment: Abandon a fraction of the worst solutions and replace them with new random
solutions.
6. Iteration: Repeat the process for a predefined number of generations.

**Task Scheduling** in cloud computing involves assigning a set of tasks to a set of virtual machines
in a way that optimizes certain perfomance metrics such as makespan(the amount of time to process all
of the tasks), efficiency and throughput. The goal is to minimize the completion time of all tasks while
efficiently utilizing the available resources.

# Implementation details
### Constants and Parameters
• NTS(Number of tasks) </br>
• NVM(Number of virtual machines)</br>
• Max-Generation(Maximum Generations)</br>
• pa(Probability of abandoning Worst Nests)</br>

### Task Execution Times
The task execution times on each VM are represented as a matrix.

### Schedule Length Calculation
The schedule length, or makespan, is the maximum completion time of all tasks. The algorithm calculates
the start time (St-Time) and finish time (Ft-Time) for each task on each VM, ensuring no overlapping
of tasks assigned to the same VM.

### Lévy Flight for Cuckoo Search
Lévy flight is used to explore the search space more effectively. It is characterized by long steps followed
by many short steps, ensuring a thorough exploration of the solution space.

### ECS (Cuckoo Search with Embedded Task Scheduling)
The ECS function initializes nests, performs Lévy flights, evaluates fitness, and applies abandonment. It
iterates over a defined number of generations to find the optimal task schedule.

### Performance Metrics
• Speedup: The ratio of the minimum execution time to the makespan. </br>
• Efficiency: Speedup divided by the number of VMs.</br>
• Throughput: The number of tasks divided by the makespan.</br>

### Results
The ECS algorithm identifies the best schedule and its corresponding makespan. </br>

Max-Generation = 100 </br>
pa = 0.25 Probability of abandoning worst nests </br>
NTS - 10 </br>
NVM - 3 </br>
Makespan - 39</br>
Speedup - 0.911 </br>
Efficiency - 0.303 </br>
Throughput - 0.294 </br>

Best schedule: [0 0 2 2 0 1 1 1 2 2]

![image](https://github.com/user-attachments/assets/a674ca81-9319-4e77-ba4c-b47e83c58856)

NTS - 10 </br>
NVM - 4 </br>
Makespan - 31</br>
Speedup - 0.193 </br>
Efficiency - 0.048 </br>
Throughput - 0.322 </br>
Best schedule: [0 1 2 0 0 1 3 3 1 3] </br>
![image](https://github.com/user-attachments/assets/bc9ba887-9e85-4507-b546-dca8f16b0725)
