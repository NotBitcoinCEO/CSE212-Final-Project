# Trees

* [Return to Welcome Page](0-welcome.md)

## Introduction

Trees are a common data structure used in computer science. A tree is a tree-like structure made up of nodes connected by pointers. The top-most node is called the root, and nodes that do not have any connections to other nodes are called leaves. The distance between two nodes is the least number of pointers that must be traversed to get from one node to the other. The level of a node is the distance between it and the root, and the height of a tree is the highest level of any node in the tree. Trees can be used to represent a variety of data, including file systems on a computer. In addition, subtrees can be created to focus on a smaller part of a larger tree.

## Binary Trees

In a binary search, the data is first compared to the value of the root node. If the value being searched for is greater than the root node's value, the search moves to the right subtree, and if it is less than the root node's value, the search moves to the left subtree. This process is repeated until the value is found or it is determined that the value does not exist in the tree. Because the number of nodes that must be searched is halved with each step of the search, binary tree searches can be performed in O(log n) time, as long as the tree is balanced.

![](/tree.jpg)

Here's an example of a Binary Tree:

```python
class Node:
  def __init__(self, value):
    self.value = value
    self.left = None
    self.right = None

class BinaryTree:
  def __init__(self):
    self.root = None

  def insert(self, value):
    new_node = Node(value)

    if self.root is None:
      self.root = new_node
    else:
      current = self.root
      while True:
        if value < current.value:
          if current.left is None:
            current.left = new_node
            break
          else:
            current = current.left
        else:
          if current.right is None:
            current.right = new_node
            break
          else:
            current = current.right

  def search(self, value):
    if self.root is None:
      return False
    
    current = self.root
    while current is not None:
      if value == current.value:
        return True
      elif value < current.value:
        current = current.left
      else:
        current = current.right
    
    return False

# Create a tree and insert values
tree = BinaryTree()
tree.insert(14)
tree.insert(9)
tree.insert(23)

# Search for value that exists in tree
print(tree.search(9))  # True

# Search for value that doesn't exist in tree
print(tree.search(7))  # False

```

Above we define two classes: 'Node' and 'BinaryTree'. The Node class represents a single node in a binary tree, which has a value and pointers to the left and right child nodes. The BinaryTree class represents a binary tree data structure, which can be used to store data in a tree-like structure.

The BinaryTree class has two methods: insert and search. The insert method takes a value and creates a new Node object with that value. It then places the new node in the correct position in the tree, according to the value of the node. The search method takes a value and searches the tree for a node with that value. It returns True if the value is found, and False otherwise.

## Operations & performance

* **insert(value)**: Adds a new value to the tree. This operation has a performance of O(log n) because it uses a recursive algorithm to insert the value in the correct position in the tree. Here's an example:

* **remove(value)**: Deletes a value from the tree. This operation also has a performance of O(log n) because it uses a recursive algorithm to find and remove the specified value from the tree. Here's an example:

* **contains(value)**: Checks if a value is part of the tree. This operation has a performance of O(log n) because it uses a recursive algorithm to search for the value in the tree.

* **traverse**: Visits each node in the tree in order, either from smallest to largest or from largest to smallest. This operation has a performance of O(n) because it needs to visit each node in the tree to complete the traversal.

* **height(node)**: Returns the height of a given node or the height of the entire tree if the root node is specified. The height of a node is the number of edges in the longest path from the node to a leaf. This operation has a performance of O(n) because it needs to visit each node in the tree to determine the height.

* **size()**: Returns the number of values in the tree. This operation has a performance of O(1) because the BST class maintains a counter that is incremented whenever a new value is inserted and decremented whenever a value is removed. This operation can also be used to check if the tree is empty by checking if the size is 0.

You can read more about binary trees here: [Python documentation](https://www.geeksforgeeks.org/binary-tree-data-structure/?ref=gcse).

## Challenge

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None
```

### Create a binary tree with a height of 3
```python
root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
root.left.right = Node(5)
root.right.left = Node(6)
root.right.right = Node(7)
```

### Calculate the height of the binary tree
```python
tree_height = height(root)
```

### Print the height of the binary tree
```python
print(tree_height)
```

* [Solution to this challenge](/solution3.md)


* [Head back to the Welcome page](0-welcome.md)
