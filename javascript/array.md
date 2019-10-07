JavaScript *arrays* are used to store multiple values in a single variable.

# Array Explanation

Array index starts from 0, i.e first item will be indexed at 0 and last will be n-1 if there are n no of items in an array

Example - 

``` js
var numbers = [1,2,3,4,5]

console.log(numbers[0]) // 1
console.log(numbers[1]) // 2

```


### `Array can also be created using`

  ``` js
  var numbers = new Array(1,2,3,4,5);
  ```

### `Changing the values`

  ``` js
  numbers[0] = 100;
  console.log(numbers[0]) // 100
  ```

### `Length of an array`

  ``` js
  console.log(numbers.length); // 5
  ```

### `Accessing First & Last item`

  ``` js
  console.log(numbers[0]); // 100 because we changed the value of the first item earlier
  console.log(numbers[numbers.length - 1]); // 5
  ```

### `Looping through an array`

  *Array.forEach()* can be used to loop through an array
  You can check it here - https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_loop_foreach

### `Adding an item to array`

  *push* is used to add an item to the array
  ``` js
  numbers.push(6);
  console.log(numbers) // [100, 2, 3, 4, 5, 6]
  ```

### `Check if variable is an array`
  
  ``` js
  typeof numbers; // returns object
  ```

  so, we need to use

    Array.isArray(numbers); // returns true

NOTE - Arrays are of "objects" type


# Array Methods

### `1) Convert array to string`

  ##### `i) Using *toString()* method`
    
    var cities = ["Bangalore", "Udupi", "Mangalore", "Coorg"];
    cities.toString(); // "Bangalore,Udupi,Mangalore,Coorg"


  ##### `ii) Using join() method - we can specify the seperator`
  
    var cities = ["Bangalore", "Udupi", "Mangalore", "Coorg"];
    cities.join(" * "); // "Bangalore * Udupi * Mangalore * Coorg"
 

### `2) Popping: pop() - this method is used to remove the last item from the array`

   
    // This returns the value that was removed

    var cities = ["Bangalore", "Udupi", "Mangalore", "Coorg"];
    cities.pop(); // "Coorg"
    console.log(cities); // ["Bangalore", "Udupi", "Mangalore"]

### `3) Pushing: push() - this method is used to add an item to the end of an array`

    // This returns the new array length

    var cities = ["Bangalore", "Udupi", "Mangalore"];
    cities.push("Coorg"); // 4
    console.log(cities); // ["Bangalore", "Udupi", "Mangalore", "Coorg"];

### `4) Shifting Elements: shift() - this method works equivalent to pop() but removes the first item of an array`

    // This returns the value that was removed

    var cities = ["Bangalore", "Udupi", "Mangalore", "Coorg"];
    cities.shift(); // "Bangalore"
    console.log(cities); // ["Udupi", "Mangalore", "Coorg"]

### `5) Unshifting Elements: unshift() - this method adds a new element to an array (at the beginning)`

    ``` js
    // This returns the new array length

    var cities = ["Bangalore", "Udupi", "Mangalore"];
    cities.unshift("Coorg"); // 4
    console.log(cities); // ["Coorg", "Bangalore", "Udupi", "Mangalore"];
    ```

### `6) Splicing an Array: splice() - this method can be used to add new items to an array or to remove items`

    // This returns an array with the deleted items

    var cities = ["Bangalore", "Udupi", "Mangalore", "Coorg"];

    cities.splice(2,0, "Mysore"); // []

    cities.splice(0,1); // ["Bangalore"]
    console.log(cities); // ["Udupi", "Mysore", "Mangalore", "Coorg"]

    Here - 
      First Parameter(2) is the position where new elements should be added
      Second Paramter(0) defines how many elements should be removed
      Rest defines the new elements to be added

### `7) Merging (Concatenating) Arrays: concat() - this method creates a new array by merging (concatenating) existing arrays`
    
    `concat()` method does not change the existing arrays. It always returns a new array & an take any number of array arguments

    var cities1 = ["Bangalore", "Coorg"];
    var cities2 = ["Udupi", "Mangalore"];
    var cities3 = ["Mysore"];
    var cities = cities1.concat(cities2, cities3); // ["Bangalore", "Coorg", "Udupi", "Mangalore", "Mysore"]

### `8) Slicing an Array: slice() - this method slices out a piece of an array into a new array.

    var cities = ["Bangalore", "Udupi", "Mangalore", "Coorg"];
    var newCities = cities.slice(1); // ["Udupi", "Mangalore", "Coorg"] Removes the first item
    var newCities = cities.slice(2); // ["Mangalore", "Coorg"] Removes the first 2 items
    var newCities = cities.slice(3); // ["Mangalore", "Coorg"] Removes the first 3 items
    var newCities1 = cities.slice(1,3); // ["Udupi", "Mangalore"] Removes the first item to second item

    This method selects elements from the start argument, and up to (but not including) the end argument,
    end argument is not taken into account if not provided

    NOTE - The array index starts from 1, not 0 unlike other array methods
