# 🔁 Queue using Linked List: Display Front and Rear Elements of a Queue

## 🎯 Aim

To write a Python program to:
- Insert elements into a queue.
- Display the element at the **front** of the queue.
- Display the element at the **rear** of the queue.

---

## 🧠 Algorithm

1. **Initialize Queue**:
   - Create an empty list called `queue`.

2. **Insert Elements**:
   - Use the `append()` method to add `'a'`, `'b'`, `'c'`, and `'d'` to the queue.

3. **Display Initial Queue**:
   - Print `"Initial Queue:"` followed by the current state of the queue.

4. **Identify Front and Rear**:
   - Set `front = queue[0]` for the front element.
   - Set `rear = queue[-1]` for the rear element.

5. **Print Results**:
   - Display the front and rear elements with appropriate messages.

---
## Program
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class Queue:
    def __init__(self):
        self.front = None
        self.rear = None
    def insert(self, data):
        new_node = Node(data)
        if self.rear is None:
            self.front = self.rear = new_node
        else:
            self.rear.next = new_node
            self.rear = new_node
        print(f"Inserted: {data}")
    def display_front(self):
        if self.front is None:
            print("Queue is empty. No front element.")
        else:
            print(f"Front element: {self.front.data}")
    def display_rear(self):
        if self.rear is None:
            print("Queue is empty. No rear element.")
        else:
            print(f"Rear element: {self.rear.data}")
if __name__ == "__main__":
    q = Queue()
    q.insert(100)
    q.insert(200)
    q.insert(300)
    q.display_front()
    q.display_rear()

## Output
<img width="619" height="204" alt="image" src="https://github.com/user-attachments/assets/b6788817-3cda-4275-95e3-639d7ba3c08c" />

## Result
Thus the program has been executed successfully.
