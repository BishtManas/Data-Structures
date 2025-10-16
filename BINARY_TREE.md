# Binary Tree — Data Structure Notes

---

## *Introduction*

A **Binary Tree** is a **hierarchical data structure** in which each node has **at most two children**:

* **Left child**  
* **Right child**  

The topmost node is called the **root**, and nodes with no children are called **leaf nodes**.  

Binary trees are widely used in **searching, sorting, and hierarchical data storage**.

---

## *Types of Binary Trees*

* **Full Binary Tree** – Every node has 0 or 2 children.  
* **Perfect Binary Tree** – All internal nodes have 2 children, all leaves at same level.  
* **Complete Binary Tree** – All levels filled except possibly last, left to right.  
* **Degenerate (or pathological) Tree** – Each parent has only one child (like a linked list).  
* **Binary Search Tree (BST)** – Left child < parent < right child for all nodes.

---

## *Basic Terminology*

* **Node** – Contains data and pointers to left and right children.  
* **Edge** – Connection between parent and child node.  
* **Level** – Distance from root (root at level 0).  
* **Height** – Longest path from root to leaf.  

---

## *Binary Tree Traversals*

* **Inorder (Left, Root, Right)**  
* **Preorder (Root, Left, Right)**  
* **Postorder (Left, Right, Root)**  
* **Level Order (Breadth First)**  

*Time Complexity:* All traversals take O(n), where n = number of nodes.

---

## *Implementation of Binary Tree in C++*

```cpp
#include <iostream>
using namespace std;

class Node {
public:
    int data;
    Node* left;
    Node* right;

    Node(int val) {
        data = val;
        left = right = nullptr;
    }
};

// Inorder Traversal
void inorder(Node* root) {
    if (root == nullptr) return;
    inorder(root->left);
    cout << root->data << " ";
    inorder(root->right);
}

// Preorder Traversal
void preorder(Node* root) {
    if (root == nullptr) return;
    cout << root->data << " ";
    preorder(root->left);
    preorder(root->right);
}

// Postorder Traversal
void postorder(Node* root) {
    if (root == nullptr) return;
    postorder(root->left);
    postorder(root->right);
    cout << root->data << " ";
}

int main() {
    Node* root = new Node(1);
    root->left = new Node(2);
    root->right = new Node(3);
    root->left->left = new Node(4);
    root->left->right = new Node(5);

    cout << "Inorder: ";
    inorder(root);
    cout << "\nPreorder: ";
    preorder(root);
    cout << "\nPostorder: ";
    postorder(root);

    return 0;
}

# Binary Tree — Applications, Advantages, and Disadvantages

---

## *Applications of Binary Tree*

* **Expression Trees** – Represent algebraic expressions.  
* **Binary Search Tree (BST)** – Fast searching, insertion, deletion.  
* **Heaps** – Used in priority queues.  
* **Huffman Encoding Trees** – Compression algorithms.  
* **Hierarchical data storage** – File systems, organizational charts.  

---

## *Advantages of Binary Tree*

* Efficient searching and sorting when structured as BST.  
* Flexible memory allocation.  
* Provides hierarchical data representation.  

---

## *Disadvantages of Binary Tree*

* Wastage of memory if tree is sparse.  
* Traversal can be recursive and memory-intensive.  
* Not cache-friendly like arrays.  
