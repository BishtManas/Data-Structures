# 🧵 **String Data Structure – Detailed Notes**

---

## 🔹 1. What is a String?

A **string** is a **sequence of characters** stored together to represent text.
It is one of the most common and important data structures used in programming.

**Example:**

```python
s = "hello"
```

Here, `s` is a string containing the characters `'h', 'e', 'l', 'l', 'o'`.

---

## 🔹 2. String Representation in Memory

* In most languages, strings are stored as **arrays of characters**.
* Each character takes up **1 byte (ASCII)** or **more (Unicode)** depending on encoding.
* A **null character (‘\0’)** is often used in languages like C to mark the **end of a string**.

**Example (C style):**

```
"hello" → ['h', 'e', 'l', 'l', 'o', '\0']
```

In Python or Java, strings are **immutable** — once created, you cannot change them.

---

## 🔹 3. Common String Operations

| Operation     | Description     | Example                | Time Complexity |
| ------------- | --------------- | ---------------------- | --------------- |
| `len(s)`      | Find length     | `len("abc") → 3`       | O(1)            |
| Concatenation | Join strings    | `"a" + "b" → "ab"`     | O(n)            |
| Slicing       | Extract part    | `"hello"[1:4] → "ell"` | O(k)            |
| Comparison    | Compare strings | `"abc" < "abd"`        | O(n)            |
| Traversal     | Iterate chars   | `for ch in s:`         | O(n)            |

---

## 🔹 4. String Immutability

In languages like **Python**, **Java**, and **C#**, strings are **immutable** — meaning you can’t change a character directly.

**Example:**

```python
s = "hello"
s[0] = 'y'  # ❌ Error
```

Instead, you must create a new string:

```python
s = "y" + s[1:]  # ✅ "yello"
```

---

## 🔹 5. String Methods (Python Examples)

| Method           | Description               | Example                              |
| ---------------- | ------------------------- | ------------------------------------ |
| `s.upper()`      | Converts to uppercase     | `"hello".upper() → "HELLO"`          |
| `s.lower()`      | Converts to lowercase     | `"HELLO".lower() → "hello"`          |
| `s.strip()`      | Removes spaces            | `" hi ".strip() → "hi"`              |
| `s.replace(a,b)` | Replace substring         | `"apple".replace("a","A") → "Apple"` |
| `s.split()`      | Splits string by spaces   | `"a b c".split() → ['a','b','c']`    |
| `s.join(list)`   | Joins list with separator | `" ".join(['a','b','c']) → "a b c"`  |
| `s.find(x)`      | Finds first index         | `"hello".find('l') → 2`              |
| `s.count(x)`     | Counts occurrences        | `"hello".count('l') → 2`             |

---

## 🔹 6. Common Algorithms on Strings

### ➤ **Reversal**

```python
s[::-1]  # reverse string
```

### ➤ **Palindrome Check**

A string that reads same forward and backward.

```python
s == s[::-1]
```

### ➤ **Anagram Check**

Two strings having same characters with same frequency.

```python
sorted(s1) == sorted(s2)
```

### ➤ **Substring Search**

Find if one string is present in another.

```python
"cat" in "concatenate"  # True
```

Or using algorithms like:

* Naive Approach – O(n*m)
* KMP Algorithm – O(n+m)
* Rabin-Karp – O(n+m)

---

## 🔹 7. Advanced String Concepts

### 🧩 **Pattern Matching Algorithms**

* **Naive Search** – Check all possible positions.
* **KMP (Knuth-Morris-Pratt)** – Uses prefix table for efficient search.
* **Rabin-Karp** – Uses hashing to find matches.
* **Boyer-Moore** – Skips unnecessary comparisons using heuristics.

---

### 🧩 **String Hashing**

Used in:

* Substring search
* Plagiarism detection
* Rolling hash algorithms

Example:
Rolling hash in **Rabin-Karp Algorithm** helps compare substrings efficiently.

---

### 🧩 **Trie Data Structure (Prefix Tree)**

* Special tree used for storing strings efficiently (especially dictionary words).
* Each node represents a character.
* Operations:

  * Insert word – O(L)
  * Search word – O(L)
  * Prefix search – O(L)

---

## 🔹 8. Applications of Strings

* Text processing and searching
* Data parsing (HTML, JSON, logs)
* Pattern recognition
* Encryption/decryption
* Compiler design (tokenization, syntax analysis)
* DNA sequence analysis

---

## 🔹 9. Time and Space Complexities (Common Tasks)

| Operation                | Average Time | Space |
| ------------------------ | ------------ | ----- |
| Traversing               | O(n)         | O(1)  |
| Concatenation            | O(n)         | O(n)  |
| Substring Search (Naive) | O(n*m)       | O(1)  |
| KMP Search               | O(n+m)       | O(m)  |
| Reverse                  | O(n)         | O(n)  |
| Compare                  | O(n)         | O(1)  |

---

## 🔹 10. Summary

| Feature            | Explanation                                           |
| ------------------ | ----------------------------------------------------- |
| Type               | Sequential collection of characters                   |
| Mutability         | Immutable in Python, Java; Mutable in C (char arrays) |
| Storage            | Contiguous memory like arrays                         |
| Important Concepts | Immutability, Slicing, Concatenation, Searching       |
| Applications       | Everywhere in text-based processing                   |

---

Would you like me to give you **short Python code examples** for all these operations (like reverse, palindrome, substring search, etc.) in a clean notebook-style format (so you can use it in VS Code or LeetCode)?
