# cs170scheduler

## The Problem
Given a list of *n* igloos to polish with id *i*, deadline *t<sub>i</sub>* in minutes, duration *d<sub>i</sub>* in minutes, and profit *p<sub>i</sub>*, provide a sequence of igloos to polish in one day (1440 minutes) that would maximize the total profit.

We make the following assumptions:

• We start scheduling polishing tasks at the 0th minute of the day.  
  
• We start the next polishing task at the same minute we finish the previous polishing task. For example, if the very first task we schedule has duration 7, it starts at minute 0 and completes at minute 7. Now, the second task starts at minute 7, and assuming it has duration 10, it ends at minute 17. 
  
• We receive whole profit for tasks that complete any time before or on their deadline. For example, if a task has duration 5 and deadline 10, we get the whole profit p for the task if we schedule it at any time before minute 5 (including at minute 5) because it would complete by minute 10. If we schedule this task at minute 6, we would complete it by minute 11, and gain profit corresponding to completing the task 1 minute late.  
  
• We can schedule tasks such that the last task completes by minute 1440, For example, we can schedule a task with duration 1 at minute 1439 since it would complete by minute 1440. But, we cannot schedule a task with duration 1 at minute 1440 since it would only complete by minute 1441.  
  
  
A more in-depth explanation and details of the project can be found in ```project_spec.pdf```.

## CS170 Competition Scheduling Algorithm

Our team's algorithm for the ```CS170: Efficient Algorithms and Intractable Problems``` Competition.

We first sort the tasks using a heuristic and then try to insert each task at the latest time step where the task would not be late, shifting each subsequent task earlier in the schedule if there was not enough space. Our heuristic was a linear function of the deadline and benefit rate where the weights were randomly chosen. Randomly choosing the weights 1000 times, we selected the schedule with the highest total benefit.

Ran using Microsoft Azure
