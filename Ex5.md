# Ex.No:5
# Ex.Name:write a C++ program to implement FCFS algorithm(no of.process p1,p2 and p3 and its burst time are 10,5 & 8) find out waiting time ,Turn Around time  & Average turn around time of the the process?
## Date:
## Aim:
To write a C++ program to implement the First-Come, First-Served (FCFS) scheduling algorithm for three processes and calculate waiting time (WT), turn around time (TAT), and average turn around time (ATAT).

## Algorithm:
STEP 1: Start the program.

STEP 2: Initialize arrays to store process IDs and their burst times.

STEP 3: Initialize arrays for waiting time (WT) and turn around time (TAT).

STEP 4: Set the waiting time for the first process as 0.

STEP 5: Calculate waiting time for each process using the formula:
WT[i] = WT[i-1] + BT[i-1]

STEP 6: Calculate turn around time for each process using the formula:
TAT[i] = WT[i] + BT[i]

STEP 7: Compute the sum of turn around times for calculating the average.

STEP 8: Calculate average turn around time (ATAT) by dividing sum of TAT by number of processes.

STEP 9: Display process IDs, burst times, waiting times, and turn around times.

STEP 10: Display the average turn around time and end the program.




## Program:
```
#include <iostream>
using namespace std;

int main()
{
    int processes[] = {1, 2, 3}; 
    int bt[] = {10, 5, 8}; 
    int n = 3; 
    int wt[n], tat[n];
    int totalWT = 0, totalTAT = 0;

    wt[0] = 0; 
    for (int i = 1; i < n; i++) 
    {
        wt[i] = wt[i - 1] + bt[i - 1];
    }

    for (int i = 0; i < n; i++) 
    {
        tat[i] = bt[i] + wt[i];
        totalWT += wt[i];
        totalTAT += tat[i];
    }

    cout << "Processes   BT time   WT time   TA time\n";
    
    for (int i = 0; i < n; i++) 
    {
        cout << "       " << processes[i] << "       " << bt[i] << "       " << wt[i] << "       " << tat[i] << endl;
    }

    cout << "Average turn around time = " << (float)totalTAT / n << endl;

    return 0;
}

```


## Output:
<img width="897" height="250" alt="{21392B55-1C4E-4661-9141-AFAF3463B619}" src="https://github.com/user-attachments/assets/a209cfb0-262e-4fa9-93a3-d42704bc8209" />



## Result:
The program successfully calculates the waiting time, turn around time, and average turn around time for all processes using FCFS scheduling.
