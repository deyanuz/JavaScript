# JavaScript Arrays 📚

This section covers **JavaScript Arrays**, explaining how to create, manipulate, and utilize arrays in various scenarios. Arrays are a fundamental part of JavaScript, used to store collections of items in a single variable and manage ordered lists of data efficiently.

## Table of Contents

1. [Arrays](#arrays)
    - 1.1 [Creating Arrays](#creating-arrays)
    - 1.2 [Accessing and Modifying Elements](#accessing-and-modifying-elements)
    - 1.3 [Basic Array Methods](#basic-array-methods)
        - 1.3.1 [Adding and Removing Elements](#adding-and-removing-elements)
        - 1.3.2 [Searching for Elements](#searching-for-elements)
        - 1.3.3 [Iterating Over Arrays](#iterating-over-arrays)
    - 1.4 [Advanced Array Methods](#advanced-array-methods)
        - 1.4.1 [Transforming Arrays](#transforming-arrays)
        - 1.4.2 [Filtering Arrays](#filtering-arrays)
        - 1.4.3 [Reducing Arrays](#reducing-arrays)
2. [Strings](#strings)
    - 2.1 [Creating Strings](#creating-strings)
    - 2.2 [Basic String Operations](#basic-string-operations)
    - 2.3 [String Methods](#string-methods)
        - 2.3.1 [Finding and Extracting Substrings](#finding-and-extracting-substrings)
        - 2.3.2 [Modifying Strings](#modifying-strings)
    - 2.4 [Advanced String Manipulation](#advanced-string-manipulation)
        - 2.4.1 [Template Literals](#template-literals)
    - 2.5 [String Object vs String Primitive](#string-object-vs-string-primitive)
3. [Resources](#resources)

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

## Basic Array Methods

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
<br>

---
<br>


## Strings

JavaScript strings are used to store and manipulate text. They can contain letters, numbers, symbols, and even spaces. Strings are immutable, meaning their characters cannot be changed after creation, but you can create modified copies.

## Creating Strings

Strings can be created using single quotes (`'...'`), double quotes (`"..."`), or backticks (`\`...\`` for template literals).

```javascript
const singleQuoteString = 'Hello';
const doubleQuoteString = "World";
const templateLiteral = `Hello, ${singleQuoteString} ${doubleQuoteString}!`; // "Hello, Hello World!"
```

## Basic String Operations

- **Accessing Characters:** Use bracket notation or the `.charAt()` method.
  
  ```javascript
  const text = "Hello";
  console.log(text[0]); // Output: H
  console.log(text.charAt(1)); // Output: e
  ```

- **Length Property:** Get the number of characters in a string.
  
  ```javascript
  console.log(text.length); // Output: 5
  ```

## String Methods

JavaScript provides a variety of methods for working with strings:

### Finding and Extracting Substrings

- **indexOf**: Returns the index of the first occurrence of a substring.
- **slice**: Extracts a section of the string.
- **substring**: Extracts characters between two indices.

```javascript
const text = "Hello, JavaScript!";
console.log(text.toUpperCase()); // Output: HELLO, JAVASCRIPT!
console.log(text.indexOf("JavaScript")); // Output: 7
console.log(text.slice(0, 5)); // Output: Hello
console.log(text.substring(7, 17)); // Output: JavaScript
```

### Modifying Strings

- **toUpperCase / toLowerCase**: Converts the string to uppercase or lowercase.
- **replace**: Replaces part of a string with another string.
- **trim**: Removes whitespace from both ends.

```javascript
const greeting = " Hello ";
console.log(greeting.trim()); // Output: "Hello"
console.log(greeting.replace("Hello", "Hi")); // Output: " Hi "
```

## Advanced String Manipulation

### Template Literals

Template literals allow for string interpolation and multiline strings, making it easier to embed expressions within strings.

```javascript
const name = "Alice";
const greeting = `Hello, ${name}! Welcome to JavaScript.`;
console.log(greeting); // Output: Hello, Alice! Welcome to JavaScript.
```

## String Object vs String Primitive


## Resources

- [JavaScript Array Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [JavaScript Array Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Instance_methods)
- [JavaScript String Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

---
