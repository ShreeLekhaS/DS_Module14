# Ex10 Applications of Queue – FCFS
## DATE: 14.03.2025
## AIM:
To write a C function to calculate the turnaround time of each process given their burst time and waiting time in First Come first Serve scheduling algorithm.
## Algorithm

1.Start the program.

2.Accept process IDs (proc[]), number of processes (n), burst times, waiting times, and an array to store turnaround times.

3.Loop through each process from index 0 to n-1.

4.For each process, calculate turnaround time as turnaround time = burst time + waiting time.

5.Store the result in the tat[] array for each process.

6.End the function by returning 0. 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

#include <stdio.h>
int turnaroundtime( int proc[], int n,int burst_time[], int wait_time[], int tat[]) {
   int i;
   for(i=0;i<n;i++)
   {
       tat[i]=burst_time[i]+wait_time[i];
   }
   return 0;
}
```


## Output:

![437105363-2ddc42eb-6fbe-4b3a-a7b8-89c8e8c244b4](https://github.com/user-attachments/assets/0e1a0806-1356-4a1d-8f29-4d6fd808fc72)



## Result:
Thus, the C function to calculate the turnaround time of each process given their burst time and waiting time in First Come first Serve scheduling algorithm is implemented successfully.
