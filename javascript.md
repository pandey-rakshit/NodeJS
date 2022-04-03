# [JavaScript](https://www.javascript.com/)

Javascript (JS) is a lightweight, interpreted, object-oriented language.
* JavaScript is a synchronous single threaded language.

## Summary

* Weakly Typed Language
    
    * No explicit type assignment
    * Data types can be switched dynamically

* Object-Oriented Language
   
    * Data can be organized in logical objects
    * Primitive and reference types

* Versatile Language

    * Runs in browser and directly on a PC / Server
    * Can perform a broad variety of tasks


---

```javascript

    var numX = 5;
    var numY = 10;

    // function to add two numbers
    function addNumber(numberX , numberY){
        return numberX + numberY;
    }

    console.log(addNumber(numX, numY));

    // output: 30
```

### [var](#var), [let](#let) and [const](#const)

<a name="var" />

### var

#### SCOPE
---

* Global scoped or function scoped. 
* The scope of the ```var``` keyword is the global or function scope. 
* It means variables defined outside the function can be accessed globally, and variables defined inside a particular function can be accessed within the function.

> #### Example 1: <br> Variable ‘a’ is declared globally. So, the scope of the variable ‘a’ is global, and it can be accessible everywhere in the program. The output shown is in the console.  

```javascript

    var a = 10
        function f(){
            console.log(a)
            // output: 10
        }
    f();
    console.log(a);
    // output: 10

```
> #### Example 2: <br> The variable ‘a’ is declared inside the function. If the user tries to access it outside the function, it will display the error. Users can declare the 2 variables with the same name using the var keyword. Also, the user can reassign the value into the var variable. The output shown in the console.

```javascript

    function f() {
        
        // It can be accessible anywhere within this function
        var a = 10;
        console.log(a)
        //  output: 10
    }
    f();

    // A cannot be accessible outside of function
    console.log(a);
    // output: ReferenceError: a is not defined

```
> #### Example 3: <br> If users use the var variable before the declaration, it initializes with the undefined value. The output is shown in the console.

```javascript

    console.log(a);
    var a = 10;

    // output: undefined
```

<a name="let" />

### let

The let keyword is an improved version of the var keyword. 

#### SCOPE
--- 
* block scoped: The scope of a let variable is only block scoped. 
* It can’t be accessible outside the particular block ({block}).

> Example 1: <br> 

```javascript
    let a = 10;
    function f() {
        let b = 9
        console.log(b); // output: 9
        console.log(a); // output: 10

    }
    f();
```

> Example 2: <br> The code returns an error because we are accessing the let variable outside the function block.
```javascript

    let a = 10;
    function f() {
        if (true) {
            let b = 9
 
            // It prints 9
            console.log(b);
        }
 
        // It gives error as it is defined in if block
        console.log(b);
    }
    f()

    // It prints 10
    console.log(a)

```

> Example 3: <br> If users use the let variable before the declaration, it does not initialize with undefined just like a var variable and return an error.
```javascript

    console.log(a); // output: Uncaught ReferenceError: Cannot access 'a' before initialization
    let a = 10;

```
<a name="const" />

### const

The const keyword has all the properties that are the same as the let keyword, except the user cannot update it.

#### SCOPE
--- 

* Block scoped: When users declare a const variable, they need to initialize it, otherwise, it returns an error. 
* The user cannot update the const variable once it is declared.

> Example 1: <br> We are changing the value of the const variable so that it returns an error.
```javascript
    const a = 10;
    function f() {
        a = 9
        console.log(a)
    }
    f();

    // output: TypeError:Assignment to constant variable.
```
> Example 2: <br> Users cannot change the properties of the const object, but they can change the value of properties of the const object.
```javascript

    const a = {
        prop1: 10,
        prop2: 9
    }
     
    // It is allowed
    a.prop1 = 3
 
    // It is not allowed
    a = {
        b: 10,
        prop2: 9
    }


    //output: Uncaught SyntaxError:Unexpected identifier
```

## Differences between var, let, and const


|                                       var                                     |                                       let                           |                                          const                                               |
|:-----------------------------------------------------------------------------:|:-------------------------------------------------------------------:|:--------------------------------------------------------------------------------------------:|
|The scope of a var variable is functional scope.                               |The scope of a let variable is block scope.                          |The scope of a const variable is block scope.                                                 |
|It can be updated and re-declared into the scope.                              |It can be updated but cannot be re-declared into the scope.          |It cannot be updated or re-declared into the scope.                                           |
|It can be declared without initialization.                                     |It can be declared without initialization.                           |It cannot be declared without initialization.                                                 |
|It can be accessed without initialization as its default value is “undefined”. |It cannot be accessed without initialization, as it returns an error.|It cannot be accessed without initialization, as it cannot be declared without initialization.|


 ## REFERENCE

* [GFG](https://www.geeksforgeeks.org/difference-between-var-let-and-const-keywords-in-javascript/)
