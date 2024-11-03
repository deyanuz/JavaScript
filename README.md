# JavaScript Arrays 📚

This section covers **JavaScript Arrays**, explaining how to create, manipulate, and utilize arrays in various scenarios. Arrays are a fundamental part of JavaScript, used to store collections of items in a single variable and manage ordered lists of data efficiently.

## Table of Contents

1. [Arrays](#arrays)
    - 1.1 [Creating Arrays](#creating-arrays)
    - 1.2 [Accessing and Modifying Elements](#accessing-and-modifying-elements)
    - 1.3 [Basic Array Methods](#basic-array-methods)
        - 1.3.1 [Adding and Removing Elements](#adding-and-removing-elements)
        - 1.3.2 [Searching for Elements](#searching-for-elements)
        - 1.3.3 [Modifying the Array](#modifying-the-array)
        - 1.3.4 [Iterating Over Arrays](#iterating-over-arrays)
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

Arrays in JavaScript can be created using array literals or the `Array` constructor. Specifically, arrays can be intialized with values at the time of declaration or the values can be passed through the `Array` object constructor to create a new array.

```javascript
const arrayLiteral = [1, 2, 3]; // using array literal
const arrayConstructor = new Array(1, 2, 3); // using array object 
```

## Accessing and Modifying Elements

Elements in arrays are accessed using their index, which starts at 0. Array elements can also be modified by reassigning values at specific indices.

```javascript
const fruits = ["apple", "banana", "cherry"];
console.log(fruits[0]); // Output: apple

// Modifying an element
fruits[1] = "orange";
console.log(fruits); // ["apple", "orange", "cherry"]
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
fruits.push("banana"); // ["apple", "banana"]
fruits.shift(); // ['banana']
fruits.unshift("apple"); // ["apple", "banana"]
```

### Searching for Elements

- **indexOf**: Returns the index of a specified element.
- **includes**: Checks if an element exists. Returns `true` if the element exists in the array and `false` if it does not exist.

```javascript
const fruits = ["apple", "banana", "cherry"];
console.log(fruits.indexOf("banana")); // Output: 1
console.log(fruits.includes("orange")); // Output: false
```

### Modidying the Array

- **slice**: Returns a shallow copy of a portion of an array into a new array selected from `start` to `end` (`end` not included). Here `start` and `end` are the indices of elements. 
  
  ```javascript
  const fruits = ['Apple', 'Banana', 'Cherry', 'Date'];
  const citrus = fruits.slice(1, 3);
  console.log(citrus); // ['Banana', 'Cherry']
  ```
    In the example snippet, indices 1 through 3 are passed to the slice method. However, the returned array contains only the elements at indices 1 and 2; it does not include the element at index end (3 in this     case). Additionally, while the elements of the returned array reference the same objects in memory as the original array, this is only relevant for arrays containing objects. If the original array contains       primitive values (like numbers or strings), the values themselves are copied. Therefore, modifying the elements in the returned array will not affect the original array if they are primitives. This behavior     is why slice is often described as creating a shallow copy.
  ---

- **splice**: Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

   ```javascript
   // syntax: splice(start, deleteCount, item1, item2, /* …, */ itemN)
  const fruits = ['Apple', 'Banana', 'Cherry', 'Date']; 
  fruits.splice(1, 0, 'Orange'); // ['Apple', 'Orange', 'Banana', 'Cherry', 'Date']
  fruits.splice(4, 1, 'Pine-apple'); // ['Apple', 'Orange', 'Banana', 'Cherry', 'Pine-apple']
  fruits.splice(2, 2, 'Strawberry'); // ['Apple', 'Orange', 'Strawberry', 'Pine-apple']
   
  // remove 2 elements starting from index 1
  fruits.splice(1, 2);  // ['Apple', 'Pine-apple']
  // remove all elements starting from index 1
  fruits.splice(1);  // ['Apple']
  ```
  `splice` first performs deletion, that is, it first deletes `deleteCount` number of items from index `start` inclusive. After that, the method inserts the items from `start` index onwards.
  ---

- **sort**: The `sort()` method sorts the elements of an array in place and returns the sorted array. By default, the `sort()` method sorts elements as strings in ascending order. When sorting numbers, this can        lead to unexpected results because the elements are converted to strings and sorted based on their Unicode values.

  ```javascript
  let fruits = ["banana", "apple", "cherry"];
  fruits.sort();
  console.log(fruits); // Output: ["apple", "banana", "cherry"]

  let numbers = [4, 2, 5, 1, 3];
  numbers.sort();
  console.log(numbers); // Output: [1, 2, 3, 4, 5] (correct order)

  // Incorrect ordering without a compare function
  let numbersIncorrect = [10, 2, 30, 1];
  numbersIncorrect.sort();
  console.log(numbersIncorrect); // Output: [1, 10, 2, 30] (incorrect)
  ```
  To sort numbers correctly, you can pass a `compareFunction`

  ```javascript
  let numbers = [10, 2, 30, 1];
  numbers.sort((a, b) => a - b); // Ascending order
  console.log(numbers); // Output: [1, 2, 10, 30]

  numbers.sort((a, b) => b - a); // Descending order
  console.log(numbers); // Output: [30, 10, 2, 1]
  ```
  ---
  
- **reverse**:The reverse() method reverses the elements of an array in place and returns the modified array. It changes the order of the elements so that the first becomes the last, and the last becomes the         first.

    ```javascript
    let numbers = [1, 2, 3, 4, 5];
    numbers.reverse();
    console.log(numbers); // Output: [5, 4, 3, 2, 1]
    ```
    ---
  
### Iterating Over Arrays

- **forEach**: Executes a function for each element.
- **map**: Creates a new array by applying a function to each element.

```javascript
const numbers = [1, 2, 3];
numbers.forEach(element => console.log(element * 2)); // 2, 4, 6
```
Each `element` in the array is passed within the callback function provided to the `forEach` method. The function performs an operation based on the function definition.

## Advanced Array Methods

### Transforming Arrays

- **map**: The `map()` method creates a **new array** by applying a given function to each element of the original array. It does **not modify** the original array and is useful for transforming data, like converting numbers or extracting specific object properties.

```javascript
const numbers = [1, 2, 3];
const squares = numbers.map(num => num * num); // [1, 4, 9]
// Original array remains unchanged: [1, 2, 3]
```

---

### Filtering Arrays

- **filter**: The `filter()` method returns a **new array** containing only the elements that pass a specified test implemented by a callback function. This method is ideal for removing unwanted elements or creating subsets based on conditions.

```javascript
const numbers = [1, 2, 3, 4];
const evens = numbers.filter(num => num % 2 === 0); // [2, 4]
// Original array remains unchanged: [1, 2, 3, 4]
```

---

### Reducing Arrays

- **reduce**: The `reduce()` method applies a function to **accumulate** array elements into a single value. It takes a callback function and an optional initial value. The callback function receives an accumulator (accumulated result) and the current value from the array.

```javascript
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((total, num) => total + num, 0); // 10
// The initial value (0) ensures that the accumulation starts from 0.
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
