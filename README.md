# Introduction to Arrays in p5.js

Arrays are a fundamental part of programming, allowing us to store multiple values in a single variable. In p5.js, arrays are useful for managing collections of data, such as coordinates, colors, or objects like sprites. 


## Things you need to know by the end of the unit

- **Array Declaration**: You can declare arrays with `[]` and initialize them with values.
- **Accessing Elements**: Use the index to retrieve or modify elements.
- **Array Methods**: Use `.push()`, `.pop()`, and `.length` to manage your arrays.
- **Loops and Arrays**: Loops are often used to iterate over arrays, especially in visual applications.

## What is an Array?

An array is a list-like structure that can store multiple values under one variable name. Each item in the array is called an **element**, and each element is accessible by its **index**. Indices in arrays start at `0`, meaning the first element is at index `0`, the second at index `1`, and so on.

## Declaring an Array

You can declare an array in the following way:

```javascript
let myArray = []; // Creates an empty array
```

You can also initialize an array with values:

```javascript
let numbers = [10, 20, 30, 40]; // Creates an array with 4 numbers
```

## Accessing Elements

To access elements in an array, you use the array name followed by the index in square brackets `[]`:

```javascript
let firstElement = numbers[0]; // Access the first element (10)
let secondElement = numbers[1]; // Access the second element (20)
```

## Directly Modifying Elements

You can change any element in an array by specifying its index:

```javascript
numbers[0] = 100; // Changes the first element to 100
```

## Using Arrays

Arrays are often used when you need to handle multiple related elements, such as positions or colors. For example, let’s use an array to draw multiple circles on the canvas.

```javascript
let xPositions = [50, 100, 150, 200]; // X coordinates for circles

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  for (let i = 0; i < xPositions.length; i++) {
    ellipse(xPositions[i], height/2, 50, 50); // Draw circles at different X positions
  }
}
```

## Array Length

The `.length` property gives you the number of elements in the array:

```javascript
let arrayLength = xPositions.length; // Gets the length of the array (4)
```

## Adding and Removing Elements

You can use methods like `.push()` to add elements to the end of an array, and `.pop()` to remove the last element.

```javascript
xPositions.push(250); // Adds 250 to the array
xPositions.pop();     // Removes the last element from the array
```

## Example: Moving Multiple Objects

In this example, we’ll create an array of `y` positions and move circles down the screen.

```javascript
let yPositions = [50, 100, 150, 200];

function setup() {
  createCanvas(400, 400);
}

function draw() {
  background(220);
  for (let i = 0; i < yPositions.length; i++) {
    ellipse(width/2, yPositions[i], 50, 50);
    yPositions[i] += 2; // Move each circle down by 2 pixels
  }
}
```



