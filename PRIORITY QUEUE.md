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
class PriorityQueue(object):
	def __init__(self):
		self.queue = []

	def __str__(self):
		return ' '.join([str(i) for i in self.queue])

	# for checking if the queue is empty
	def isEmpty(self):
		return len(self.queue) == 0

	# for inserting an element in the queue
	def insert(self, data):
		self.queue.append(data)
		#-----CODE HERE-----
		

	# for popping an element based on Priority
	def delete(self):
	    for i in self.queue:
	        if max(self.queue)==i:
	            x=i
	            self.queue.remove(i)
	            return x
	
		#-----CODE HERE-----
			


myQueue = PriorityQueue()
n=int(input())	
for i in range(0, n):
    ele = int(input())
    myQueue.insert(ele)
	
print(myQueue)		
while not myQueue.isEmpty():
	print(myQueue.delete())

```

### OUTPUT
![image](https://github.com/user-attachments/assets/6ce430f5-64d1-43d6-8285-2f4d75014b22)

### RESULT
Successfully  wrote a Python program for simple implementation of Priority Queue using Queue.
