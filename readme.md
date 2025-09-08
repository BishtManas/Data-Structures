# 📘 **Linked List – Easy and Detailed Notes**

---

## 🔹 What is a Linked List?

A **Linked List** is a **linear data structure** where elements are **connected using pointers**.
Each element is called a **Node**.

Unlike arrays, **linked lists do not store data in a continuous memory block**. Instead, each element (node) stores:

* **Data**
* **A pointer (or reference)** to the **next node**

---

## 🧱 Structure of a Node

Each **Node** in a linked list has two parts:

```
+-----------+-----------+
|   Data    |   Next    |
+-----------+-----------+
```

* **Data** → The actual value stored (like 10, 20, "A", etc.)
* **Next** → A reference (pointer) to the **next node**

---

## 🧵 Types of Linked Lists

1. ### **Singly Linked List**

   * Each node points to the **next node** only.
   * Last node’s next is **NULL** (means end of list).
   * **One-way direction**.

   **Example:**

   ```
   [10 | next] → [20 | next] → [30 | NULL]
   ```

2. ### **Doubly Linked List**

   * Each node has **two pointers**:

     * One for the **next** node
     * One for the **previous** node
   * Can move in **both directions** (forward and backward).

   **Example:**

   ```
   NULL ← [10] ↔ [20] ↔ [30] → NULL
   ```

3. ### **Circular Linked List**

   * In this, the **last node points back to the first node**.
   * Can be singly or doubly circular.

   **Example (Singly Circular):**

   ```
   [10] → [20] → [30] → [10] (back to start)
   ```

---

## 📌 Why Use Linked Lists?

✅ Dynamic size – Can grow or shrink during runtime
✅ Efficient insertions/deletions (better than arrays)
❌ Slower access to elements (no index like in arrays)

---

## 🔄 Basic Operations in Linked List

| Operation     | Meaning                           |
| ------------- | --------------------------------- |
| **Traversal** | Visit each node one by one        |
| **Insertion** | Add a new node                    |
| **Deletion**  | Remove a node                     |
| **Searching** | Find a node with a specific value |

---

## 🔧 How Operations Work

### 1. Traversal (Printing All Elements)

Go from the head (first node), and keep going to the next until NULL.

```c
Node* temp = head;
while(temp != NULL) {
    printf("%d ", temp->data);
    temp = temp->next;
}
```

---

### 2. Insertion

**At Beginning:**

* Create a new node
* Point its next to current head
* Make new node the new head

**At End:**

* Traverse till last node
* Point last node’s next to new node

**In Middle (after some node):**

* Adjust next pointers accordingly

---

### 3. Deletion

**At Beginning:**

* Point head to next node
* Free/delete the old head

**At End:**

* Go to second last node
* Set its next to NULL
* Free/delete last node

**In Middle:**

* Find the previous node
* Change its next pointer
* Delete the desired node

---

## ✍️ Example in C (Singly Linked List)

```c
struct Node {
    int data;
    struct Node* next;
};

// Creating a new node
struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
newNode->data = 10;
newNode->next = NULL;
```

---

## 🧠 Key Terms

| Term        | Meaning                           |
| ----------- | --------------------------------- |
| **Node**    | Basic element with data + pointer |
| **Head**    | First node in the linked list     |
| **NULL**    | End of list (no next node)        |
| **Pointer** | Variable that stores address      |

---

## ✅ Advantages of Linked List

* Dynamic size
* Easy insertion and deletion
* No need to shift elements

---

## ❌ Disadvantages of Linked List

* Uses more memory (for pointers)
* No random access (can’t directly jump to an element)
* More complex than arrays

---

## 🧪 Linked List vs Array

| Feature   | Array          | Linked List          |
| --------- | -------------- | -------------------- |
| Size      | Fixed          | Dynamic              |
| Memory    | Continuous     | Not continuous       |
| Insertion | Costly (shift) | Easy (just pointers) |
| Access    | Fast (index)   | Slow (traverse)      |

---

## 📊 Real Life Examples

* Music playlist (each song linked to next)
* Browser history (back and forward using doubly list)
* Image viewer (next and previous)
