# Functional Programming :

INPUT -> PROCESS -> OUTPUT 

* __Isolated functions__ - there is no dependence on the state of the program, which includes global variables that are subject to change 
* __Pure functions__ - the same input always gives the same output 
* __Functions with limited side effects__ - any changes, or mutations, to the state of the program outside the function are carefully controlled. 

* __Callbacks__ are the functions that are slipped or passed into another function to decide the invocation of that function.  

Functions that can be assigned to a variable, passed into another function, or returned from another function just like any other normal value, are called __first class functions__. 

* In JavaScript all functions are first class. 

The functions that take a function as an argument, or return a function as a return value are called __higher order functions__. 

* When functions are passed in to or returned from another function, then those functions which were passed in or returned can be called a `lambda`. 


 __Imperative style__ in programming is one that gives the computer a set of __statements__ to perform a task. 


In contrast, __Functional programming__ is a form of __declarative programming__. You tell the computer what you want done by calling a method or function. 

    Recall that in functional programming, changing or altering things is called mutation, and the outcome is called a side effect. A function, ideally, should be a pure function, meaning that it does not cause any side effects. 


## Array.prototype.map() or map()

The ` map method` iterates over each item in an array and returns a new array containing the results of calling the callback function on each element. It does this without mutating the original array. 
[MDN Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) 

```
const users = [
    {name: 'John', age: 34},
    {name: 'Amy', age: 20},
    {name: 'camperCat', age: 10}
];
const names = users.map(user => user.name);
console.log(names); //console would display the value ['John','Amy','camperCat'].
}
```

`map` is a pure function, and its output depends solely on its inputs.  

it takes another function as its argument. 

## Filter() or Array.prototype.filter() 

`filter` calls a function on each element of an array and returns a new array containing only the elements for which that function returns **true**.  

`filter` filters the array, based on the function passed to it. Like `map`, it does this without needing to modify the original array. 
[MND Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter )

*`ParseFloat()` function parses a string and returns a float

The `slice method` returns a copy of certain elements of an array. It can take two arguments, the first gives the index of where to begin the slice, the second is the index for where to end the slice (and it's non-inclusive). 

```
var arr = ["Cat","Dog","Tiger","Zebra"];
var newArray = arr.slice(1,3); //newArray would have the value ["Dog","Tiger"]
```


**Concatenation** means to join items end to end. JavaScript offers the **concat** method for both strings and arrays that work in the same way. 

```
[1,2,3].concat([4,5,6]);

// returned array would be [1,2,3,4,5,6]
```
Note: we can use `concat()` instead of `push()`.

## Sort : 

The `sort method` sorts the elements of an array according to the callback function.

* JavaScript's default sorting method is by string** Unicode** point value, which may return unexpected results. Therefore, it is encouraged to provide a callback function to specify how to sort the array items.
* When such a callback function, normally called **compareFunction**, is supplied, the array elements are sorted according to the return value of the compareFunction
    * If compareFunction(a,b) returns a value **less than 0** for two elements a and b, then a will come before b.
    * If compareFunction(a,b) returns a value **greater than 0**for two elements a and b, then b will come before a.
    * compareFunction(a,b) returns a value **equal to 0** for two elements a and b, then a and b will remain unchanged.

```
var str = "Hello World";
var bySpace = str.split(" ");

// bySpace would have value ["Hello", "World"]
```

`join() mathod` is used to join the elements of an array together to create a string. 
it takes an argument for delimiter that is used toseperate the array elments in the string.

```
var arr = ["Hello","World"];
var str = arr.join(" ");

// str would have value of string "Hello World"
```

The `every method` works with arrays to check if **every** element passes a particular test. It returns a Boolean value - **true** if all values meet the criteria, **false** if not. 

 

 

The `some method` works with arrays to check if **any** element passes a particular test. It returns a Boolean value - **true** if any of the values meet the criteria, **false** if not.

## CURRYING :

The **arity** of a function is the number of arguments it requires. **Currying** a function means to convert a function of N arity into N functions of arity 1 

* it restructures a function so it takes one argument, then returns another function that takes the next argument, and so on. 

```
function unCurried(x,y){
    return x+y;
}
function curried(x){
    return function(y){
        return x + y;
    }
}
const curried = x => y => x+y;
curried(1)(2)  // return 3
```

## Partial Application : 

Similarly, *partial application* can be described as applying a few arguments to a function at a time and returning another function that is applied to more arguments. 

```
function impartial(x,y,z){
    return x + y + z;
}
var partialFn = impartial.bind(this, 1, 2);
partialFn(10); // 13
```