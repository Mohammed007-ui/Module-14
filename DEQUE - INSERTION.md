# Exp.No:39  
## DEQUE - INSERTION

---

### AIM  
To write a Python program to insert elements at REAR END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Initialize an empty deque.  
3. Start an infinite loop using `while True`.  
4. In each iteration, take input from the user.  
5. If the input is an empty string, break the loop.  
6. If the input is not empty, convert it to an integer and append it to the deque.  
7. After the loop ends, append the values `14` and `15` to the deque.  
8. Print the message `"The deque after appending at right is :"`.  
9. Print the contents of the deque.  

---

### PROGRAM  

```
from collections import deque

# Initialize deque with some elements
dq = deque()

# Input initial values to the deque
for _ in range(3):
    value = int(input())
    dq.append(value)

# Insert 14 and 15 at the rear end
dq.append(14)
dq.append(15)

# Display the deque contents
print("The deque after appending at right is :")
print(dq)

```

### OUTPUT
![image](https://github.com/user-attachments/assets/9c2ee7fa-b9fd-455c-8fab-216669409d40)

### RESULT
 successfully wrote a Python program to insert elements at REAR END of deque using a collection built-in function.

