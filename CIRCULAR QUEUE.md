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
class CircularQueue:
    def __init__(self, max_size):
        self.queue = [None] * max_size
        self.max_size = max_size
        self.head = 0
        self.tail = 0
        self.size = 0

    def insert(self, value):
        if self.size == self.max_size:
            print("Queue is full. Cannot insert", value)
            return
        try:
            value = float(value)
            self.queue[self.tail] = value
            print(f"Inserted {value} at position {self.tail}")
            self.tail = (self.tail + 1) % self.max_size
            self.size += 1
        except ValueError:
            print("Invalid float value.")

    def display(self):
        print("Queue contents:")
        i = self.head
        count = 0
        while count < self.size:
            print(self.queue[i], end=" ")
            i = (i + 1) % self.max_size
            count += 1
        print()


# Example usage:
cq = CircularQueue(5)

cq.insert(2.3)
cq.insert(4.5)
cq.insert(6.7)
cq.insert(8.9)
cq.insert(1.1)
cq.display()

# Try inserting into a full queue
cq.insert(9.9)


```

### OUTPUT
![image](https://github.com/user-attachments/assets/be403aac-340a-425f-b2ed-7e0d9055819f)


### RESULT
The program successfully demonstrates insertion of float values into a circular queue using circular indexing.
