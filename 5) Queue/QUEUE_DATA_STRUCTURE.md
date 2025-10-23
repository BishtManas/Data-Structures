# Queue — Data Structure Notes

## Introduction
A **Queue** is a **linear data structure** that follows the **FIFO (First In First Out)** principle.  
The first element inserted is the first one to be removed.  
It can be visualized as people standing in a line: the person at the front is served first.

---

## Basic Operations on Queue
* **enqueue(x)** → Insert element `x` at the rear of the queue.  
* **dequeue()** → Remove the element from the front of the queue.  
* **peek() / front()** → Return the element at the front without removing it.  
* **isEmpty()** → Check if the queue is empty.  
* **isFull()** → Check if the queue is full (for fixed-size array implementation).  

*Time Complexity:* All operations are O(1) on average.

---

## Implementation of Queue using Array (C++)

```cpp
#include <iostream>
#define MAX 100
using namespace std;

class Queue {
    int front, rear;
    int arr[MAX];

public:
    Queue() {
        front = -1;
        rear = -1;
    }

    bool enqueue(int x) {
        if (rear == MAX - 1) {
            cout << "Queue Overflow\n";
            return false;
        }
        if (front == -1) front = 0;
        arr[++rear] = x;
        return true;
    }

    int dequeue() {
        if (front == -1 || front > rear) {
            cout << "Queue Underflow\n";
            return -1;
        }
        return arr[front++];
    }

    int peek() {
        if (front == -1 || front > rear) {
            cout << "Queue is Empty\n";
            return -1;
        }
        return arr[front];
    }

    bool isEmpty() {
        return (front == -1 || front > rear);
    }
};

int main() {
    Queue q;
    q.enqueue(10);
    q.enqueue(20);
    q.enqueue(30);
    cout << q.dequeue() << " dequeued\n";
    cout << "Front element: " << q.peek() << endl;
    return 0;
}
