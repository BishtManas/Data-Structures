# 📚 Array Data Structure

Arrays are one of the most **basic and important data structures**. If you’re starting your journey in Data Structures and Algorithms (DSA), arrays are usually the first concept you’ll learn.

---

## 🔹 What is an Array?

An **array** is a collection of elements stored at **contiguous (continuous) memory locations**.

* All elements are of the **same data type** (e.g., all integers, all floats, all characters).
* You can access elements using their **index**.
* The first element has index **0**, the second has index **1**, and so on.

👉 Think of an array as a row of lockers in a school — each locker has an address (index), and you can store one item in each locker.

---

## 🔹 Why do we need Arrays?

✅ To store multiple values in a **single variable** instead of creating separate variables.

✅ To access elements **quickly using index**.

✅ To efficiently perform operations like sorting, searching, and traversing.

Example without array:

```c
int a1 = 10, a2 = 20, a3 = 30, a4 = 40;
```

Example with array:

```c
int arr[4] = {10, 20, 30, 40};
```

---

## 🔹 Key Features of Arrays

1. **Fixed Size** – Once declared, the size of the array cannot be changed.
2. **Same Data Type** – All elements should be of the same type.
3. **Index Based Access** – Directly access any element with its index.
4. **Efficient Traversal** – Easy to loop through all elements.

---

## 🔹 Types of Arrays

1. **One-Dimensional Array (1D Array)**

   * A simple list of elements.
   * Example: `int arr[5] = {1, 2, 3, 4, 5};`

2. **Two-Dimensional Array (2D Array)**

   * Like a matrix or table (rows × columns).
   * Example:

     ```
     1 2 3
     4 5 6
     7 8 9
     ```

3. **Multi-Dimensional Array**

   * More than 2 dimensions, like a 3D cube.

---

## 🔹 Common Array Operations

| Operation     | Description                                                      | Time Complexity |
| ------------- | ---------------------------------------------------------------- | --------------- |
| **Traversal** | Visit each element one by one                                    | O(n)            |
| **Insertion** | Add a new element (at end = O(1), middle = O(n))                 | O(n)            |
| **Deletion**  | Remove an element (end = O(1), middle = O(n))                    | O(n)            |
| **Searching** | Find an element (Linear Search = O(n), Binary Search = O(log n)) | Depends         |
| **Updation**  | Change the value of an element                                   | O(1)            |

---

## 🔹 Example in C (1D Array)

```c
#include <stdio.h>

int main() {
    int arr[5] = {10, 20, 30, 40, 50};  // Declare and initialize array

    printf("Array elements:\n");
    for (int i = 0; i < 5; i++) {
        printf("%d ", arr[i]);  // Access using index
    }
    return 0;
}
```

---

## 🔹 Example in Python

```python
# In Python, lists work like arrays
arr = [10, 20, 30, 40, 50]

print("Array elements:")
for i in range(len(arr)):
    print(arr[i], end=" ")
```

---

## 🔹 Real-Life Examples of Arrays

* 📱 Contact list in your phone (names stored in order).
* 🎶 Playlist of songs.
* 🏫 Student roll numbers in a class.
* 🎮 Game scores.

---

## 🔹 Advantages of Arrays

* Easy to use and understand.
* Fast access using index.
* Useful for implementing other data structures (stack, queue, matrix).

---

## 🔹 Limitations of Arrays

* Fixed size (cannot grow/shrink easily).
* Insertion/Deletion in the middle is slow.
* Wastes memory if not fully used.

---

## 🚀 Summary

* Arrays store **similar data** at **continuous memory locations**.
* Index starts from **0**.
* Operations like traversal, searching, insertion, deletion are common.
* Used everywhere in programming (from apps to games to databases).

👉 **Mastering arrays is the first step to becoming good at Data Structures and Algorithms (DSA).**