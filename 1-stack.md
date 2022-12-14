# Stacks

* [Return to Welcome Page](0-welcome.md)

## Introduction

 Imagine a stack of pancakes, with the first pancake that was made at the bottom and the most recently made pancake on the top. When someone takes a pancake, they take it from the top of the stack. This is similar to the undo function in a program, where the most recently added element can be easily removed without disrupting the rest of the elements in the stack. In other words, a stack is a data structure that follows the order of Last In First Out (LIFO) or First In Last Out (FILO).

 ![](/images/stack.jpg)

Stacks have efficient performance with operations that run in O(1) time. The most common stack operations are push, which adds a new element to the top of the stack, pop, which removes and returns the element on the top of the stack, and size, which returns the number of elements in the stack. In Python, these operations can be performed using the following code:

```python
stack = [] # create empty stack

# push element to stack
stack.append(10)

# pop element from stack
popped_element = stack.pop()

# get size of stack
stack_size = len(stack)

```
Another common operation for stacks is peek, which returns the element on the top of the stack without removing it. This can be implemented in Python as follows:

```python

def peek(stack):
    if len(stack) != 0:
        return stack[-1]
    else:
        return None

pancakes = [1, 2, 3]
top_pancake = peek(pancakes) # returns 3

```

In this code, the function peek() takes a stack as an argument and checks if the stack is empty. If it is not empty, it returns the last element in the stack (the element on the top of the stack). If the stack is empty, it returns None.

In the example, we create a stack of pancakes with three elements and use the peek() function to return the top element of the stack (the element with value 3 in this case).

Overall, stacks are a useful data structure for storing and manipulating data in a LIFO or FILO order. They have efficient performance and can be used in various applications, such as the undo function in a program.

#Challenge

```python
# Initialize an empty stack
stack = []

# Push three numbers onto the stack
stack.append(3)
stack.append(2)
stack.append(1)

# Pop one number from the stack
stack.pop()

# Push two new numbers onto the stack
stack.append(4)
stack.append(5)

# What is the current top element of the stack?
```
You can read more about stacks here: [Python documentation](https://www.geeksforgeeks.org/stack-in-python/).

* [Solution to this challenge](/code/solution1.md)

* [Head back to the Welcome page](0-welcome.md)

![](/images/pancakes.jpg)