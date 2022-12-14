# Sets

* [Return to Welcome Page](0-welcome.md)

## Introduction

In Python, sets are a data type that allows you to store unique values without maintaining their order. Sets are different from lists because they do not allow duplicates and do not maintain the order of the values they contain.

Sets use a process called hashing to efficiently store and retrieve values in O(1) time. Hashing involves transforming a value into a simpler representation that specifies its position in the set. In Python, the built-in hash() function can be used for this purpose.

Here's an example of how to create a set and add values to it in Python:

```python
# create empty set
my_set = set()

# add values to set
my_set.add(1)
my_set.add(3)
my_set.add(5)

# print set to see contents
print(my_set)
```
This code will create a set called my_set and add the values 1, 3, and 5 to it. When you print the set, you'll see that it contains only those values and does not maintain their order:

```python
{1, 3, 5}
```

You can also use keyword to check if a value is present in a set. For example:

```python
# check if the value 1 is in the set
print(1 in my_set)

# check if the value 2 is in the set
print(2 in my_set)
```
This code will print True for the first in statement because the value 1 is in the set, and False for the second in statement because the value 2 is not in the set.

## Challenge

Write a Python function called unique_elements that takes in a list of numbers and returns a new list containing only the unique elements from the original list. Your solution must use the set() function to solve this problem.

Here is an example of how your function should work:

```python
# Original list
numbers = [1, 2, 3, 3, 4, 4, 5, 6, 7, 7]

# Call function
unique_nums = unique_elements(numbers)

# Print result
print(unique_nums)
```
Your function should print the following output:

[1, 2, 3, 4, 5, 6, 7]


There are many other operations that you can perform on sets in Python, such as removing values from the set, calculating the union or intersection of two sets, and more. You can read more about sets here: [Python documentation](https://www.geeksforgeeks.org/sets-in-python/).

* [Head back to the Welcome page](0-welcome.md)

![](/set.jpg)
