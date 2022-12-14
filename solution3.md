# Solution 3

![](/binary.jpg)

```python
class Node:
    def __init__(self, val):
        self.val = val
        self.left = None
        self.right = None

root = Node(5)
root.left = Node(2)
root.right = Node(7)
root.right.left = Node(6)
root.right.right = Node(8)
```

## Find max value in tree
```python
max_val = find_max(root)
```

## Answer
```python
print(max_val) # outputs 8
```
