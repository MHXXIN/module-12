# 📚 Stack using Linked List: Stack Implementation (Top Element Display)

## 🎯 Aim

To write a Python program that implements a **stack**.  
The program allows inserting 3 elements from the user and then prints the **top element** of the stack.

---

## 🧠 Algorithm

1. **Start the program.**
2. **Initialize** an empty list called `stack` to simulate the stack.
3. **Repeat 3 times**:
   - Prompt the user to **input a value**.
   - Use `stack.append(value)` to **push** the value onto the stack.
4. After inserting 3 elements:
   - Access the **top element** using `stack[-1]`.
5. **Print** the top element.
6. **End the program.**

---

## 💻 Program
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class Stack:
    def __init__(self):
        self.top = None
    def push(self, data):
        new_node = Node(data)
        new_node.next = self.top
        self.top = new_node
    def display_top(self):
        if self.top is None:
            print("Stack is empty.")
        else:
            print(f"🔝 Top element: {self.top.data}")
if __name__ == "__main__":
    stack = Stack()
    for i in range(3):
        value = input(f"Enter element {i+1}: ")
        stack.push(value)
    stack.display_top()
## Output
<img width="550" height="196" alt="image" src="https://github.com/user-attachments/assets/4fb52da4-94cb-4da2-a829-284fe1020fcf" />

## Result
Thus the program has been executed successfully.
