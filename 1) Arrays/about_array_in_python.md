# **Array data structures in Python**

First thing to know:

* Python doesn’t have a built-in “array” type like C or Java.
* But it gives us **lists**, **array module**, and **NumPy arrays** to work with.

Here are examples of each 👇

---

### 1. **Using Python List as Array**

Lists are the most common array-like structure in Python.

```python
# Creating an array using list
arr = [10, 20, 30, 40, 50]

# Accessing elements
print(arr[0])   # 10
print(arr[2])   # 30

# Updating element
arr[1] = 25
print(arr)      # [10, 25, 30, 40, 50]

# Adding element
arr.append(60)
print(arr)      # [10, 25, 30, 40, 50, 60]

# Removing element
arr.remove(30)
print(arr)      # [10, 25, 40, 50, 60]
```

---

### 2. **Using `array` Module**

If you want a real array (fixed type, like in C), Python has an `array` module.

```python
import array

# Create an integer array
arr = array.array('i', [1, 2, 3, 4, 5])

# Access elements
print(arr[0])   # 1
print(arr[2])   # 3

# Insert element
arr.insert(2, 99)
print(arr)      # array('i', [1, 2, 99, 3, 4, 5])

# Remove element
arr.remove(4)
print(arr)      # array('i', [1, 2, 99, 3, 5])
```

(`'i'` means integer type. Other codes exist like `'f'` for float.)

---

### 3. **Using NumPy Array** (for big data/scientific work)

NumPy arrays are very powerful for math and large data.

```python
import numpy as np

# Create NumPy array
arr = np.array([1, 2, 3, 4, 5])

# Access elements
print(arr[0])   # 1
print(arr[3])   # 4

# Vectorized operation (fast math)
print(arr * 2)  # [ 2  4  6  8 10]

# Slicing
print(arr[1:4]) # [2 3 4]
```

---

👉 So in short:

* **List** → flexible, most common in Python.
* **array module** → fixed type arrays (closer to C).
* **NumPy arrays** → best for numerical/matrix operations.