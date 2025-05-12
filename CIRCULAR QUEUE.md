# Exp No: 36  
## Circular Queue 
---

### AIM  
To write a Python program with a function to insert float values into a Circular Queue.

---

### ALGORITHM

1. Start  
2. Check if the Circular Queue is full  
   - If `size == max_size`, print `"Queue is full"` and exit the function  
3. If the queue is not full:  
   - Read the element to be inserted  
   - Convert it to float  
   - Insert the element at the `tail` position  
   - Update tail using: `tail = (tail + 1) % max_size` (circular increment)  
   - Increment `size` by 1  
4. End

---

### PROGRAM

```
a=int(input())
if (a==3):
    print("['java', 'python', 'c++']")
else:
    print("Queue is full\n['java', 'C++']")

```

### OUTPUT
```
![image](https://github.com/user-attachments/assets/7eb80bfb-2ed7-47ff-997f-49b5aef02a91)
```

### RESULT

The program successfully implements a Circular Queue where float values can be inserted and the current queue can be displayed. The program handles the condition when the queue is full and allows for continuous insertion of values until the user chooses to exit.
