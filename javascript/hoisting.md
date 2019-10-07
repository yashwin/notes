# Javascript Hoisting

### `Explanation`

Hoisting is Javascript's default of moving varible declarations to the top.

Example - 

  ``` js
  a = 1;
  console.log(a); // 1
  var a;
  ```

Here variable can be used before it has been declared

Javascript moves all the declarations to the top of the current scope (to the top of the current script or the current function)

#### `NOTE - let and const are not hoisted`

### `Initializations are Not Hoisted`

In Javascript, only declarations are hoisted, but initializations are not.

Example -

  ``` js
  var x = 1;
  console.log(x, y, z); // 1 undefined and  `Uncaught ReferenceError: z is not defined`
  var y = 7;

  var x = 5;
  var y;
  console.log(x, y); // 1 undefined
  y = 7;
  ```

