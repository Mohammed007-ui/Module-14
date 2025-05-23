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
from collections import deque

# Create an empty deque
dq = deque()

# Number of elements to input
n = 3

print(f"Enter {n} integers to add to the deque:")

# Input elements and append to deque
for _ in range(n):
    while True:
        try:
            value = int(input())
            dq.append(value)
            break
        except ValueError:
            print("Please enter a valid integer.")

print("Deque before deletion:", dq)

# Remove element from front
if dq:
    removed_element = dq.popleft()
    print(f"Removed element from front: {removed_element}")
else:
    print("Deque is empty, nothing to remove.")

print("Deque after deletion:", dq)

```

### OUTPUT
![image](https://github.com/user-attachments/assets/48440da4-f2a8-460d-8fba-dd64671f93f1)


### RESULT
The program successfully deletes the front element from the deque and displays the updated deque.

