# Stack Data Structure

## Introduction
A **stack** is a linear data structure that follows the **Last In, First Out (LIFO)** principle. In a stack, the last element added is the first one to be removed. Think of it like a stack of plates: you add and remove plates from the top only.

## Characteristics
- **LIFO Structure:** Last element inserted is the first to be removed.
- **Operations are performed at one end** called the **top**.
- **Dynamic or Static:** A stack can be implemented using arrays (static) or linked lists (dynamic).

## Basic Operations
1. **Push** – Adds an element to the top of the stack.
2. **Pop** – Removes the element from the top of the stack.
3. **Peek/Top** – Returns the top element without removing it.
4. **isEmpty** – Checks if the stack is empty.
5. **isFull** – Checks if the stack is full (only in array implementation).

## Implementation

### Using Array (Python Example)
```python
class Stack:
    def __init__(self, max_size):
        self.stack = []
        self.max_size = max_size

    def isEmpty(self):
        return len(self.stack) == 0

    def isFull(self):
        return len(self.stack) == self.max_size

    def push(self, item):
        if self.isFull():
            print("Stack Overflow")
        else:
            self.stack.append(item)
            print(f"Pushed {item} to stack")

    def pop(self):
        if self.isEmpty():
            print("Stack Underflow")
        else:
            item = self.stack.pop()
            print(f"Popped {item} from stack")
            return item

    def peek(self):
        if self.isEmpty():
            print("Stack is empty")
        else:
            return self.stack[-1]

# Example usage
stack = Stack(5)
stack.push(10)
stack.push(20)
print(stack.peek())  # Output: 20
stack.pop()
