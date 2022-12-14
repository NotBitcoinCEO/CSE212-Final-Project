# Solution 2

To solve this problem, you will need to use the set() function to create a set of unique numbers, and then use a loop to convert the set back into a list. Here is some starter code to help you get started:

```python
def unique_elements(nums):
  unique_nums = set(nums)

  # Create new list
  unique_nums_list = []

  # Loop
  for num in unique_nums:
    # Append
    unique_nums_list.append(num)

  # Return new list
  return unique_nums_list

```
Once you have written your function, you can test it by running the code below. If your function is correct, the code should print the output shown above.

```python
# The original list
numbers = [1, 2, 3, 3, 4, 4, 5, 6, 7, 7]

# Call function
unique_nums = unique_elements(numbers)

# Print the result
print(unique_nums)
```