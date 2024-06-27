# 20.2.0-python-lists


### Introduction to Arrays in Python

Arrays, also known as lists in Python, are fundamental data structures that allow you to store and manipulate collections of values. 
To create a list in Python, you can use the following syntax:

```python
my_list = []  # creates an empty list
```

You can also initialize a list with elements:

```python
my_list = [1, 2, 3, 4, 5]  # creates a list with 5 elements
```

You can access elements in a list using square brackets and the index of the element. Remember that list indices start from 0:

```python
value = my_list[2]  # accesses the third element in the list
```

You can modify elements in a list using the index as well:

```python
my_list[0] = 10  # changes the first element to 10
```

Lists also have many built-in functions and methods that you can use to manipulate them. Some common ones include:

- `len()`: function that returns the number of elements in the list.
- `append()`: method that adds an element to the end of the list.
- `pop()`: method that removes and returns the last element from the list.
- `insert()`: method that inserts an element at a specified position in the list.
- `extend()`: method that extends the list by appending elements from another list.

Here's an example of using some of these list methods in Python:

```python
my_list = [1, 2, 3]

print(len(my_list))  # prints 3

my_list.append(4)  # adds 4 to the end of the list
print(my_list)  # prints [1, 2, 3, 4]

my_list.pop()  # removes the last element from the list
print(my_list)  # prints [1, 2, 3]

my_list.insert(1, 5)  # inserts 5 at index 1
print(my_list)  # prints [1, 5, 2, 3]

another_list = [6, 7]
my_list.extend(another_list)  # extends my_list by appending elements from another_list
print(my_list)  # prints [1, 5, 2, 3, 6, 7]
```
