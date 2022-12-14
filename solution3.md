# Solution 3

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

* Create a binary tree with a height of 3
```

```python
root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
root.left.right = Node(5)
root.right.left = Node(6)
root.right.right = Node(7)
```

* Calculate the height of the binary tree

```python
tree_height = height(root)
```

* Print the height of the binary tree

```python
print(tree_height)
```

* ANSWER: 2