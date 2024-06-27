# 20.2.0-Intro-to-arrays

### Introduction to Arrays 
Arrays are a fundamental data structure that allow you to store and manipulate collections of values. They are commonly used for storing positional data, color values, and more complex data structures in creative coding projects.

To create an array in p5.js, you can use the following syntax:

```javascript
let myArray = []; // creates an empty array
```

You can also initialize an array with elements:

```javascript
let myArray = [1, 2, 3, 4, 5]; // creates an array with 5 elements
```

You can access elements in an array using square brackets and the index of the element. Remember that array indices start from 0:

```javascript
let value = myArray[2]; // accesses the third element in the array
```

You can modify elements in an array using the index as well:

```javascript
myArray[0] = 10; // changes the first element to 10
```

Arrays also have many built-in properties and methods that you can use to manipulate them. Some common ones include:

- `length`: property that returns the number of elements in the array.
- `push()`: method that adds one or more elements to the end of the array.
- `pop()`: method that removes the last element from the array.
- `splice()`: method that can add or remove elements from specified positions in the array.
- `concat()`: method that joins two or more arrays together.

Here's an example of using some of these array methods in a p5.js sketch:

```javascript
let myArray = [1, 2, 3];

print(myArray.length); // prints 3

myArray.push(4); // adds 4 to the end of the array
print(myArray); // prints [1, 2, 3, 4]

myArray.pop(); // removes the last element from the array
print(myArray); // prints [1, 2, 3]

myArray.splice(1, 1); // removes one element starting from index 1
print(myArray); // prints [1, 3]

let newArray = myArray.concat([4, 5]); // concatenates (fancy way of saying joins) myArray with [4, 5] 
print(newArray); // prints [1, 3, 4, 5]
```

