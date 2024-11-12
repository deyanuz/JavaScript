## Arrays in JavaScript
In JavaScript, arrays aren't primitives but are instead `Array` objects. They have certain distinctive properties such as:
+ JavaScript arrays are resizable and can contain a mix of different data types.

+ JavaScript array-copy operations create shallow copies ( meaning that a new array or object is created, but the elements or properties are not fully copied; instead, references to the original elements or objects are shared ). 

+ JavaScript arrays are zero-indexed. Elements of an array can be accessed using nonnegative integers (or their respective string form) as indexes.


## Constructor

The Array constructor in JavaScript is used to create a new array. It can be called in different ways:

```javascript
let arr1 = new Array(3); // [ , , ] (array with 3 empty slots)
let arr2 = new Array(1, 2, 3); // [1, 2, 3]
```

### *Using `Array` Constructor for Iteration*

The `Array` constructor can be used creatively to run a block of code a specified number of times without using a traditional loop.

 ```javascript
 Array(3).fill().map(e => {
     console.log("hi");
 });

 /* Output : hi
             hi
             hi
 */
 ```
 Array(3) creates an array with 3 empty slots. `fill()` fills all slots with `undefined`, making it easier to iterate. `map()` iterates over the array. The value of `e` is `undefined` for each iteration. This     is being used to execute the code inside map 3 times, printing "hi" each time. This approach serves as an alternative to a standard for loop.



## Creating Arrays

Arrays in JavaScript can be created using array literals or the `Array` constructor. Specifically, arrays can be initialized with values at the time of declaration or the values can be passed through the `Array` object constructor to create a new array.

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

### *Adding and Removing Elements*

- **<u>push</u> :** Adds elements to the end.
- **<u>pop</u> :** Removes the last element.
- **<u>shift</u> :** Removes the first element.
- **<u>unshift</u> :** Adds elements to the beginning.

```javascript
const fruits = ["apple"];
fruits.push("banana"); // ["apple", "banana"]
fruits.pop(); // ["apple"]
fruits.push("banana"); // ["apple", "banana"]
fruits.shift(); // ['banana']
fruits.unshift("apple"); // ["apple", "banana"]
```

### *Searching for Elements*

- **<u>indexOf</u> :** Returns the index of a specified element.
- **<u>includes</u> :** Checks if an element exists. Returns `true` if the element exists in the array and `false` if it does not exist.

```javascript
const fruits = ["apple", "banana", "cherry"];
console.log(fruits.indexOf("banana")); // Output: 1
console.log(fruits.includes("orange")); // Output: false
```

### *Modifying the Array*

- **<u>slice</u> :** Returns a shallow copy of a portion of an array into a new array selected from `start` to `end` (`end` not included). Here `start` and `end` are the indices of elements. 
  
```javascript
 const fruits = ['Apple', 'Banana', 'Cherry', 'Date'];
 const citrus = fruits.slice(1, 3);
 console.log(citrus); // ['Banana', 'Cherry']
 ```
   In the example snippet, indices 1 through 3 are passed to the slice method. However, the returned array contains only the elements at indices 1 and 2; it does not include the element at index end (3 in this     case). Additionally, while the elements of the returned array reference the same objects in memory as the original array, this is only relevant for arrays containing objects. If the original array contains       primitive values (like numbers or strings), the values themselves are copied. Therefore, modifying the elements in the returned array will not affect the original array if they are primitives. This behavior     is why slice is often described as creating a shallow copy.
  
  ---

<br>


- **<u>splice</u> :** Changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

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
`splice` first performs deletion, that is, it first deletes `deleteCount`number of items from index `start` inclusive. After that, the method inserts the items from `start` index onwards.

---

<br>


- **<u>sort</u> :** The `sort()` method sorts the elements of an array in place and returns the sorted array. By default, the `sort()` method sorts elements as strings in ascending order. When sorting numbers, this can        lead to unexpected results because the elements are converted to strings and sorted based on their Unicode values.

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

<br>

  
- **<u>reverse</u> :** The `reverse()` method reverses the elements of an array in place and returns the modified array. It changes the order of the elements so that the first becomes the last, and the last becomes the         first.

```javascript
    let numbers = [1, 2, 3, 4, 5];
    numbers.reverse();
    console.log(numbers); // Output: [5, 4, 3, 2, 1]
```
---

<br>


- **<u>fill</u> :** The `fill()` method of changes all elements within a range of indices in an array to a static value. It returns the modified array.

```javascript
     const array1 = [1, 2, 3, 4];
    
    // Fill with 0 from position 2 until position 4
    console.log(array1.fill(0, 2, 4)); // Output: [1, 2, 0, 0]

    // Fill with 5 from position 1
    console.log(array1.fill(5, 1)); // Output: [1, 5, 5, 5]
    console.log(array1.fill(6)) // Output: [6, 6, 6, 6]
```
---

<br>

  
## Iterating Over Arrays

- **<u>forEach</u> :** Executes a function for each element.
- **<u>map</u> :** Creates a new array by applying a function to each element.

```javascript
const numbers = [1, 2, 3];
numbers.forEach(element => console.log(element * 2)); // 2, 4, 6
```
Each `element` in the array is passed within the callback function provided to the `forEach` method. The function performs an operation based on the function definition.

<br>



## Advanced Array Methods

### *Transforming Arrays*

- **<u>map</u> :** The `map()` method creates a **new array** by applying a given function to each element of the original array. It does **not modify** the original array and is useful for transforming data, like converting numbers or extracting specific object properties.

```javascript
const numbers = [1, 2, 3];
const squares = numbers.map(num => num * num); // [1, 4, 9]
// Original array remains unchanged: [1, 2, 3]
```

---

### Filtering Arrays

- **<u>filter</u> :** The `filter()` method returns a **new array** containing only the elements that pass a specified test implemented by a callback function. This method is ideal for removing unwanted elements or creating subsets based on conditions.

```javascript
const numbers = [1, 2, 3, 4];
const evens = numbers.filter(num => num % 2 === 0); // [2, 4]
// Original array remains unchanged: [1, 2, 3, 4]
```

---

### Reducing Arrays

- **<u>reduce</u> :** The `reduce()` method applies a function to **accumulate** array elements into a single value. It takes a callback function and an optional initial value. The callback function receives an accumulator (accumulated result) and the current value from the array.

```javascript
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((total, num) => total + num, 0); // 10
// The initial value (0) ensures that the accumulation starts from 0.
``` 