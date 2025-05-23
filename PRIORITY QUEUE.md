# Exp.No:37  
## PRIORITY QUEUE

---

### AIM  
To write a Python program for simple implementation of Priority Queue using Queue.

---

### ALGORITHM

1. Start the program.  
2. Define a class `PriorityQueue` with an initializer to create an empty list `queue`.  
3. Define the `__str__` method to return queue elements as a string separated by spaces.  
4. Define the `isEmpty()` method to check if the queue is empty.  
5. Define the `insert(data)` method to append the given data to the queue.  
6. Define the `delete()` method to:  
   - Initialize `max_val` as 0.  
   - Loop through the queue and find the index of the maximum value.  
   - Delete and return the element at that index.  
7. In the main code, take integer input `n` for number of elements.  
8. Loop `n` times to take input values and insert them into the priority queue.  
9. Print the contents of the queue.  
10. While the queue is not empty, call `delete()` and print each returned element.  
11. End the program.

---

### PROGRAM

```
class PriorityQueue:
    def __init__(self):
        self.queue = []

    def __str__(self):
        return ' '.join(str(i) for i in self.queue)

    def isEmpty(self):
        return len(self.queue) == 0

    def insert(self, data):
        self.queue.append(data)

    def delete(self):
        if self.isEmpty():
            return None
        max_val = self.queue[0]
        max_index = 0
        for i in range(1, len(self.queue)):
            if self.queue[i] > max_val:
                max_val = self.queue[i]
                max_index = i
        return self.queue.pop(max_index)

# Main program
pq = PriorityQueue()
n = int(input("Enter the number of elements to insert in Priority Queue: "))

print(f"Enter {n} elements:")
for _ in range(n):
    val = int(input())
    pq.insert(val)

print("Queue contents:", pq)

print("Deleting elements based on priority:")
while not pq.isEmpty():
    print(pq.delete(), end=' ')
print()

```

### OUTPUT
![image](https://github.com/user-attachments/assets/de2e00f8-c95e-4aa5-b2af-77db28f5e600)

### RESULT
The program implements a priority queue where elements are inserted normally and deleted in order of highest priority (highest value first). It successfully inserts, displays, and deletes elements in priority order.

