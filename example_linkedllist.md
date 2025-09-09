## 🌱 What is a Linked List?

A **Linked List** is a way to **store a collection of elements** (like numbers or words), where each element (called a **node**) points to the **next one** in the list.

It's like a **chain** where each link connects to the next one.

---

## 🔗 Structure of a Node

Each **node** in a linked list has **two parts**:

1. **Data** – the actual value (like a number or a word)
2. **Pointer (next)** – a reference (or link) to the **next node**

```
+------+------+
| Data | Next |
+------+------+
```

For example:

```
+------+------+
|  10  |  o---> (points to next node)
+------+------+
```

---

## 📋 Types of Linked Lists

1. **Singly Linked List**
2. **Doubly Linked List**
3. **Circular Linked List**

We'll start with **Singly Linked List** (most basic).

---

## 🧱 Singly Linked List Example

Let’s create a simple linked list with 3 elements: **10 → 20 → 30**

### Step-by-Step:

### 🔹 Node 1

```
Data: 10
Next: address of Node 2
```

### 🔹 Node 2

```
Data: 20
Next: address of Node 3
```

### 🔹 Node 3

```
Data: 30
Next: NULL (means end of the list)
```

### 📊 Diagram:

```
+------+------    +------+------    +------+------+
| 10   |  o-----> | 20   |  o-----> | 30   | NULL |
+------+------    +------+------    +------+------+
```

---

## ✅ Basic Operations

Let’s understand the **basic operations** in a singly linked list.

---

### 1️⃣ **Creating a Node (in C-like pseudocode)**

```c
struct Node {
    int data;
    struct Node* next;
};
```

---

### 2️⃣ **Inserting a Node at the Beginning**

Before:

```
Head → 10 → 20 → 30
```

Add `5` at the beginning:

```c
newNode->data = 5;
newNode->next = head;
head = newNode;
```

After:

```
Head → 5 → 10 → 20 → 30
```

---

### 3️⃣ **Inserting at the End**

Before:

```
Head → 10 → 20 → 30
```

Add `40` at the end:

Steps:

* Traverse to last node (`30`)
* Make `30.next = newNode`
* Set `newNode.next = NULL`

After:

```
Head → 10 → 20 → 30 → 40
```

---

### 4️⃣ **Traversing a Linked List**

To print all values:

```c
Node* temp = head;
while (temp != NULL) {
    printf("%d ", temp->data);
    temp = temp->next;
}
```

Output:

```
10 20 30
```

---

### 5️⃣ **Deleting a Node**

Let’s delete `20`:

Steps:

* Traverse to node before 20 (i.e., 10)
* Make `10.next = 30`

Before:

```
10 → 20 → 30
```

After:

```
10 → 30
```

---

## 🌀 Doubly Linked List (Brief Intro)

Each node has **three parts**:

1. Previous pointer
2. Data
3. Next pointer

```
NULL ← [10] ↔ [20] ↔ [30] → NULL
```

Used when you want to go **both forward and backward** in the list.

---

## 🔄 Circular Linked List (Brief Intro)

Last node connects back to the **first** node.

```
10 → 20 → 30 → back to 10
```

No `NULL`, it’s a **loop**.

---

## 💡 Why Use Linked List?

| Array                       | Linked List                                  |
| --------------------------- | -------------------------------------------- |
| Fixed size (needs resizing) | Flexible size                                |
| Insert/delete is expensive  | Insert/delete is easy (just change pointers) |
| Random access (fast)        | No random access (slow traversal)            |

---

## 🧠 Final Example in Python

Here’s a working example of a simple singly linked list in **Python**:

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insert(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" → ")
            temp = temp.next
        print("NULL")

# Create a linked list
ll = LinkedList()
ll.insert(30)
ll.insert(20)
ll.insert(10)

ll.display()
```

**Output:**

```
10 → 20 → 30 → NULL
```

---

## 📝 Summary

* A **Linked List** is made of **nodes**
* Each node has **data + pointer**
* Easier to insert/delete elements than arrays
* Comes in different types: **Singly**, **Doubly**, **Circular**
