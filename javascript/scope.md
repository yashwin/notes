# Javascript Scope

Scope determines the accessibility (visibility) of variables. Variable defined inside a function are not accessible (visible) from outside the function.

### `Function Scopes`

Javascript has function scope - Each function creates a new scope

2 Types

  ##### `i) Local Scope

  Variables declared within a JavaScript function, become LOCAL to the function. Local variables have Function scope. They can only be accessed from within the function. 

  Example -

    ```js
    // `city` cannot be accessed here
    function myCity() {
      var city = "Udupi";
      // `city` can be accessed here
    }
    // `city` cannot be accessed here
    ```
  You redefine the variable `city` in other scope(different function)

  Local variables are created when a function starts, and deleted when the function is completed.

  ##### `ii) Global Scope

  Variable declared outside a function, becomes GLOBAL. A global variable has global scope: All scripts and functions on a web page can access it. 

  Example -

    ```js
    var city = "Udupi";
    // `city` can be accessed here
    function myCity() {
      
      // `city` can be accessed here
    }
    // `city` can be accessed here
    ```
  
    

