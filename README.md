# cs170scheduler

Details of the project can be found in ```project_spec.pdf```.

## CS170 Competition Scheduling Algorithm

Our team's algorithm for the ```CS170: Efficient Algorithms and Intractable Problems``` Competition.

We first sort the tasks using a heuristic and then try to insert each task at the latest time step where the task would not be late, shifting each subsequent task earlier in the schedule if there was not enough space. Our heuristic was a linear function of the deadline and benefit rate where the weights were randomly chosen. Randomly choosing the weights 1000 times, we selected the schedule with the highest total benefit.
