# JavaScript Arrays 📚

This section covers **JavaScript Arrays**, explaining how to create, manipulate, and utilize arrays in various scenarios. Arrays are a fundamental part of JavaScript, used to store collections of items in a single variable and manage ordered lists of data efficiently.

## Table of Contents

1. [Arrays](#arrays)
2. [Creating Arrays](#creating-arrays)
3. [Accessing and Modifying Elements](#accessing-and-modifying-elements)
4. [Array Methods](#array-methods)
    - 4.1 [Adding and Removing Elements](#adding-and-removing-elements)
    - 4.2 [Searching for Elements](#searching-for-elements)
    - 4.3 [Iterating Over Arrays](#iterating-over-arrays)
5. [Advanced Array Methods](#advanced-array-methods)
    - 5.1 [Transforming Arrays](#transforming-arrays)
    - 5.2 [Filtering Arrays](#filtering-arrays)
    - 5.3 [Reducing Arrays](#reducing-arrays)
6. [Examples](#examples)
7. [Resources](#resources)

---

## Arrays

JavaScript arrays are used to store multiple values in a single variable, allowing us to manage ordered lists of data. Arrays can contain any data type, including numbers, strings, objects, or even other arrays.

## Creating Arrays

Arrays in JavaScript can be created using array literals or the `Array` constructor.

```javascript
const arrayLiteral = [1, 2, 3];
const arrayConstructor = new Array(1, 2, 3);
```

## Accessing and Modifying Elements

Elements in arrays are accessed using their index, which starts at 0. Array elements can also be modified by reassigning values at specific indices.

```javascript
const fruits = ["apple", "banana", "cherry"];
console.log(fruits[0]); // Output: apple

// Modifying an element
fruits[1] = "orange"; // ["apple", "orange", "cherry"]
```

## Array Methods

JavaScript provides many built-in methods for working with arrays:

### Adding and Removing Elements

- **push**: Adds elements to the end.
- **pop**: Removes the last element.
- **shift**: Removes the first element.
- **unshift**: Adds elements to the beginning.

```javascript
const fruits = ["apple"];
fruits.push("banana"); // ["apple", "banana"]
fruits.pop(); // ["apple"]
```

### Searching for Elements

- **indexOf**: Returns the index of a specified element.
- **includes**: Checks if an element exists.

```javascript
const fruits = ["apple", "banana", "cherry"];
console.log(fruits.indexOf("banana")); // Output: 1
console.log(fruits.includes("orange")); // Output: false
```

### Iterating Over Arrays

- **forEach**: Executes a function for each element.
- **map**: Creates a new array by applying a function to each element.

```javascript
const numbers = [1, 2, 3];
numbers.forEach(num => console.log(num * 2)); // 2, 4, 6
```

## Advanced Array Methods

### Transforming Arrays

- **map**: Returns a new array by applying a function to each element.

```javascript
const numbers = [1, 2, 3];
const squares = numbers.map(num => num * num); // [1, 4, 9]
```

### Filtering Arrays

- **filter**: Creates a new array with elements that pass a specific test.

```javascript
const numbers = [1, 2, 3, 4];
const evens = numbers.filter(num => num % 2 === 0); // [2, 4]
```

### Reducing Arrays

- **reduce**: Reduces the array to a single value based on a function.

```javascript
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((total, num) => total + num, 0); // 10
```

## Examples

Explore the `examples` folder for additional code samples demonstrating how to use arrays in practical scenarios.

## Resources

- [JavaScript Array Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [JavaScript Array Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Instance_methods)

---
