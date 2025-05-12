# Exp.No:38  
## Deque - DELETION

---

### AIM  
To write a Python program to delete elements at FRONT END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Create an empty deque.  
3. Define how many elements to input (e.g., 3 inputs as in the example).  
4. Loop through the range of input size:  
   - Read an integer from the user.  
   - Append the integer to the deque.  
5. Remove the front element of the deque using `popleft()`.  
6. Print the final deque after deletion.  

---

### PROGRAM  

```

def CalculateWaitingTime(at, bt, N):

	wt = [0]*N;


	wt[0] = 0;

	print("P.No.\tArrival Time\t" , "Burst Time\tWaiting Time");
	print("1" , "\t\t" , at[0] , "\t\t" , bt[0] , "\t\t" , wt[0]);

	for i in range(1,5):
	    wt[i] = (at[i-1] + bt[i-1] +wt[i-1])-at[i];


	    print(i + 1 , "\t\t" , at[i] , "\t\t" , bt[i] , "\t\t" , wt[i]);
	average = 0.0;
	sum = 0;
	for i in range(5):
	    sum=sum+wt[i];
	   
	average=sum/5

	print("Average waiting time = ",average);

N = 5;

at = [ 0, 1, 2, 3, 4 ];


bt=[]
for i in range(0, 5):
    ele = int(input())
    bt.append(ele)

CalculateWaitingTime(at, bt, N);



```

### OUTPUT
![image](https://github.com/user-attachments/assets/dbba452d-1fc4-44d6-a80b-be98750ea15c)


### RESULT
Successfully wrote a Python program to delete elements at FRONT END of deque using a collection built-in function.

