# Ex9 Applications of Queue - SJF
## DATE:
## AIM:
To incorporate the code to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm.
## Algorithm

1.Start the program and take input for the number of processes and their burst times.

2.Assign process IDs and sort all processes in ascending order of burst time (SJF scheduling).

3.Set the waiting time of the first process to 0.

4.Calculate waiting time for each process by summing the burst times of all previous processes.

5.Compute turnaround time for each process as: turnaround time = waiting time + burst time.

6.Display the burst, waiting, and turnaround times along with their averages.   

## Program:
```
/*
Program to find the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm.
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/

#include<stdio.h>
int main()
{
    int bt[20],p[20],wt[20],tat[20],i,j,n,total=0,pos,temp;
    float avg_wt,avg_tat;
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&bt[i]);
        p[i]=i+1;    
    }

    for(i=0;i<n;i++)
    {
        pos=i;
        for(j=i+1;j<n;j++)
        {
            if(bt[j]<bt[pos])
                pos=j;
        }
 
        temp=bt[i];
        bt[i]=bt[pos];
        bt[pos]=temp;
 
        temp=p[i];
        p[i]=p[pos];
        p[pos]=temp;
    }
    wt[0]=0;
    for(i=1;i<n;i++)
    {
        wt[i]=0;
        for(j=0;j<i;j++)
        {
            wt[i]+=bt[j];
        }
        total+=wt[i];
    }
    avg_wt=(float)total/n;
    
    total=0;
 
    printf("Process    Burst Time    Waiting Time  Turnaround Time\n");
    for(i=0;i<n;i++)
    {
        tat[i]=bt[i]+wt[i];
        total+=tat[i];
        printf("p%d      %d      %d        %d\n",p[i],bt[i],wt[i],tat[i]);
    }
 
    avg_tat=(float)total/n;
    printf("Average Waiting Time=%f\n",avg_wt);
    printf("Average Turnaround Time=%f\n",avg_tat);
    return 0;
}

```

## Output:

![image](https://github.com/user-attachments/assets/df1a964e-1a48-477a-8803-1bbd3a90975d)



## Result:
Thus, the code to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm is implemented successfully.
