# JavaScript Arrays 📚

This section covers **JavaScript Arrays**, explaining how to create, manipulate, and utilize arrays in various scenarios. Arrays are a fundamental part of JavaScript, used to store collections of items in a single variable and manage ordered lists of data efficiently.

---

## Date Object

The `Date` object is used for working with dates and times. It provides methods to create, manipulate, and format dates.

### Creating a Date

- **Syntax**: You can create a `Date` object using different constructors.

  ```javascript
  const now = new Date(); // Current date and time
  const specificDate = new Date(2024, 0, 1); // January 1, 2024 (month is 0-indexed)
  const fromString = new Date("2024-11-03T12:00:00"); // Date from string
  ```

  The `Date` object can represent the current time or specific dates. The month parameter is zero-based, so January is `0`.

### Getting Date Information

- **getFullYear / getMonth / getDate**: Methods to get specific parts of a date.

  ```javascript
  const date = new Date(2024, 10, 3); // November 3, 2024
  console.log(date.getFullYear()); // Output: 2024
  console.log(date.getMonth()); // Output: 10 (November)
  console.log(date.getDate()); // Output: 3
  ```

  `getFullYear` returns the year, `getMonth` returns the zero-based month, and `getDate` returns the day of the month.

### Setting Date Information

- **setFullYear / setMonth / setDate**: Methods to set parts of a date.

  ```javascript
  const date = new Date();
  date.setFullYear(2025);
  date.setMonth(5); // June (0-indexed)
  date.setDate(15);
  console.log(date); // Updated date: June 15, 2025
  ```

  Use `setFullYear`, `setMonth`, and `setDate` to modify date values. These methods change the `Date` object in place.

<br>

---

<br>

## Math Object

The `Math` object provides mathematical constants and functions. It has no constructor and is used directly.

### Common Math Methods

- **Math.round / Math.ceil / Math.floor**: Rounds a number to the nearest integer.

  ```javascript
  console.log(Math.round(4.6)); // Output: 5
  console.log(Math.ceil(4.2)); // Output: 5
  console.log(Math.floor(4.8)); // Output: 4
  ```

  `Math.round` rounds to the nearest integer, `Math.ceil` rounds up, and `Math.floor` rounds down.

### Mathematical Constants

- **Math.PI / Math.E**: Constants representing π and Euler's number.

  ```javascript
  console.log(Math.PI); // Output: 3.141592653589793
  console.log(Math.E); // Output: 2.718281828459045
  ```

  Use `Math.PI` for calculations involving circles and `Math.E` for exponential calculations.

### Other Math Methods

- **Math.max / Math.min**: Returns the largest or smallest number from a set.
- **Math.random**: Generates a random number between 0 (inclusive) and 1 (exclusive).

  ```javascript
  console.log(Math.max(1, 3, 2)); // Output: 3
  console.log(Math.min(1, 3, 2)); // Output: 1

  let numbers = [10, 2, 30, 1];
  console.log(Math.max(...numbers)); // Output: 30

  console.log(Math.random()); // Output: Random number (e.g., 0.235)
  ```

  In the third code snippet, the `...` is used to spread its elements as individual arguments.

---

### Logarithmic Functions

- **Math.log / Math.log10 / Math.log2**: Compute the natural logarithm, base-10 logarithm, and base-2 logarithm of a number.

  ```javascript
  console.log(Math.log(1)); // Output: 0 (natural logarithm of 1)
  console.log(Math.log10(100)); // Output: 2 (log base 10 of 100)
  console.log(Math.log2(8)); // Output: 3 (log base 2 of 8)
  ```

  ***

### Trigonometric Functions

- **Math.sin / Math.cos / Math.tan**: Compute the sine, cosine, and tangent of an angle (in radians).

  ```javascript
  console.log(Math.sin(Math.PI / 2)); // Output: 1 (sine of 90 degrees)
  console.log(Math.cos(0)); // Output: 1 (cosine of 0 degrees)
  console.log(Math.tan(Math.PI / 4)); // Output: 1 (tangent of 45 degrees)
  ```

  ***

  ### Hyperbolic Functions

- **Math.sinh / Math.cosh / Math.tanh**: Compute the hyperbolic sine, cosine, and tangent of a number.

  ```javascript
  console.log(Math.sinh(1)); // Output: 1.1752011936438014
  console.log(Math.cosh(0)); // Output: 1
  console.log(Math.tanh(1)); // Output: 0.7615941559557649
  ```

  ***

## Resources

- [JavaScript Date Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)
- [JavaScript Math Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)

---
