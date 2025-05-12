# Exp.No:40  
## APPLICATIONS OF QUEUE

---

### AIM  
To write a Python program to implement CPU Process Scheduling using a queue.

---

### ALGORITHM  

1. Start the program.  
2. Define the function `CalculateWaitingTime(at, bt, N)`.  
3. Initialize a list `wt` of size `N` with all values set to 0.  
4. Set `wt[0] = 0` for the first process.  
5. Print the table header: "P.No.", "Arrival Time", "Burst Time", "Waiting Time".  
6. Print the values for the first process.  
7. For each process from index `1` to `N-1`:  
   - Calculate `wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]`.  
   - Print the process number, arrival time, burst time, and waiting time.  
8. Initialize `total_waiting_time = 0`.  
9. Add up all waiting times.  
10. Calculate average waiting time as `average = total_waiting_time / N`.  
11. Print the average waiting time.  
12. Get burst times as input from the user for 5 processes.  
13. Call `CalculateWaitingTime()` with `at`, `bt`, and `N`.  
14. End the program.

---

### PROGRAM  

```
def CalculateWaitingTime(at, bt, N):
    wt = [0] * N
    wt[0] = 0
    print("\nP.No.\tArrival Time\tBurst Time\tWaiting Time")
    for i in range(1, N):
        wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]
        print(f"{i+1}\t{at[i]}\t\t{bt[i]}\t\t{wt[i]}")
    total_waiting_time = sum(wt)
    average = total_waiting_time / N
    print(f"\nAverage Waiting Time: {average:.2f}")

def main():
    N = 5
    at = [0] * N
    bt = [0] * N
    print("Enter the Arrival Times and Burst Times for 5 processes:")
    for i in range(N):
        at[i] = int(input(f"Enter Arrival Time for Process {i+1}: "))
        bt[i] = int(input(f"Enter Burst Time for Process {i+1}: "))
    CalculateWaitingTime(at, bt, N)

if __name__ == "__main__":
    main()

```

### OUTPUT
![image](https://github.com/user-attachments/assets/e37de618-bdeb-4cdf-85fc-e11c74fae326)


### RESULT
The program successfully calculates the waiting times for each process, the average waiting time, and handles the CPU Process Scheduling using a queue. The input consists of arrival times and burst times, and the output is displayed in a tabular form.
