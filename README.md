# Intro to Arrays (aka lists)

- Arrays are essential for managing collections of related data. Understanding arrays is a fundamental skill for any programmer.
- Arrays allow us to store multiple values in a single variable, making it easier to manage and manipulate data.
- Arrays simplify data management and reduce the need for repetitive code. Imagine manually handling a list of numbers or strings without arrays!

As you start learning to work with arrays, it's important to grasp the following concepts:
- **Array Initialization**: making lists
- **Array Indexing**: what is the number of each item
- **Array Methods**: the fancy way to say, manipulate lists
- **Iterating Over Arrays**: running over each item in the list

## Before We Start

There are a few key terms you need to know by the end of this unit:
- **Array**
- **Element**
- **Index**
- **Length**
- **Push**
- **Pop**
- **Splice**
- **Slice**

# 1.1 Array Basics

First, run this code:

```javascript
let numbers = [1, 2, 3, 4, 5];// pre-fill a list
console.log(numbers); // prints [1, 2, 3, 4, 5]. if you want to see the whole list
console.log(numbers[0]); // prints 1. This is how we access each element in a list 
console.log(numbers.length); // prints 5, how many elements are in the list. Import for making for loops
```
This code initializes an array named `numbers` with five elements and prints the array, the first element, and the length of the array.

## Adding Items to an Array by Index

You can add items to an array at specific index positions using array assignment. Here's how:

```javascript
let fruits = ['apple', 'banana', 'cherry'];// starter
console.log(fruits); // prints ['apple', 'banana', 'cherry']

fruits[1] = 'orange';// I want to change bananas to oranges
console.log(fruits); // prints ['apple', 'orange', 'cherry']
```

or add a full list using index numbers
```javascript
let movies = []; // empty list to start
movie[0] = "James Bond"
movie[1] = "Inception"
movie[2] = "Avengers: Endgame"
movie[3] = "Forrest Gump"

```

- **Array Assignment**: Assigning a value to a specific index of an array updates the element at that index.
- In the example above, `fruits[1] = 'orange';` replaces the element at index `1` (which is 'banana') with 'orange'.

### Important Points:

- An array is created using square brackets `[]`, with elements separated by commas.
- Array elements are accessed using indices, starting from 0.
- The `length` property returns the number of elements in the array.

# Adding/Removing Elements to/from the End of the List

```javascript
let fruits = ['apple', 'banana', 'cherry'];
console.log(fruits); // prints ['apple', 'banana', 'cherry']

fruits.push('date');
console.log(fruits); // prints ['apple', 'banana', 'cherry', 'date']

let lastFruit = fruits.pop();
console.log(lastFruit); // prints 'date'
console.log(fruits); // prints ['apple', 'banana', 'cherry']
```

## Explanation of `push` and `pop`

- **`push(element)`**: Adds the specified element to the end of the array.
  ```javascript
  let array = [1, 2, 3];
  array.push(4);
  console.log(array); // prints [1, 2, 3, 4]
  ```
- **`pop()`**: Removes and returns the last element of the array.
  ```javascript
  let array = [1, 2, 3];
  let lastElement = array.pop();
  console.log(lastElement); // prints 3
  console.log(array); // prints [1, 2]
  ```

# Iterating Over Arrays

Here is an example of how to go over every item in a list using a for loop:

```javascript
let numbers = [1, 2, 3, 4, 5];
for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}
```

## Explanation of Array Length and Using it in For Loops

- **`length` Property**: The `length` property of an array returns the number of elements in that array.
  ```javascript
  let array = [10, 20, 30];
  console.log(array.length); // prints 3
  ```

- **Using `length` in For Loops**: You can use the `length` property to iterate over all elements in an array using a for loop. Here's how:
  ```javascript
  let numbers = [1, 2, 3, 4, 5];
  for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]); // prints each element in numbers array
  }
  ```
  - `numbers.length` ensures the loop runs exactly as many times as there are elements in the `numbers` array.
  - `i < numbers.length`: The loop continues as long as the index `i` is less than the length of the array `numbers`.
  - `i++`: Increments the index `i` after each iteration to access the next element in the array.

# Array Methods

Array methods are predefined functions in programming languages that work on arrays.

They let you manipulate, iterate over, and manage array elements efficiently. 
They are essential because they provide convenient ways to perform common tasks on arrays without manually coding complex algorithms.

# `splice` and `slice`

```javascript
let colors = ['red', 'green', 'blue'];
colors.splice(1, 1, 'yellow');
console.log(colors); // prints ['red', 'yellow', 'blue']

let subColors = colors.slice(1, 2);
console.log(subColors); // prints ['yellow']
```

## Explanation of `splice` and `slice`

- **`splice(start, deleteCount, item1, item2, ...)`**: Changes the contents of an array by removing or replacing existing elements and/or adding new elements.
  ```javascript
  let array = [1, 2, 3, 4];
  array.splice(1, 2, 'a', 'b');
  console.log(array); // prints [1, 'a', 'b', 4]
  ```
  - `start`: The index at which to start changing the array.
  - `deleteCount`: The number of elements to remove.
  - `item1, item2, ...`: The elements to add to the array.

- **`slice(start, end)`**: Returns a shallow copy of a portion of an array into a new array object.
  ```javascript
  let array = [1, 2, 3, 4];
  let subArray = array.slice(1, 3);
  console.log(subArray); // prints [2, 3]
  ```
  - `start`: The beginning index of the specified portion of the array.
  - `end`: The end index (not included) of the specified portion of the array.

## Key Points:

- `splice` modifies the original array, while `slice` returns a new array without modifying the original array.
- `splice` can add or remove elements, while `slice` only extracts a portion of the array.

