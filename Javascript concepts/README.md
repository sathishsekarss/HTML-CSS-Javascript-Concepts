Table of contents
1. [Variable declaration](#variable-declaration)
2. [Number objects](#number-objects)
3. [String in Javascript](#string-in-javascript)
    - [Common string methods](#common-string-methods)
4. [Arrays in javascript](#arrays-in-javascript)
	- [Adding items to the array](#adding-items-to-the-array)
	- [Removing items from the array](#removing-items-from-the-array)
	- [Loops for arrays](#loops-for-arrays)
5. [Functions in javascript](#functions-in-javascript)
6. [Classes in Javascript](#classes-in-javascript)
7. [public fields in javascript](#public-fields-in-javascript)
8. [Diamond problem in Javascript](#diamond-problem-in-javascript)
9. [promises in javascript](#promises-in-javascript)
10. [async and await in javascript](#async-and-await-in-javascript)
11. [promise chaining in javascript](#promise-chaining-in-javascript)
12. [Composition in promises](#composition-in-promises)
## Variable declaration
Types of variable declaration: let, var, and const

it is always preferred to use the “let” keyword instead of the “var” keyword for declaring variables.

Variables hoisting: It means calling the variable even before it is declared. It will throw “undefined” message.

## Number objects

Everything that deals with numbers in javascript is of type “number”. For example, you either declare var with 200 or 200.24 with floating digits type.  It is of type number.

some common methods with number object:

numberobject.tofixed(2) -> it rounds the number to decimal places.

Number(“23423”) -> we pass the number as string and returns the number in digits.  It is not a method, it is a constructor.

>[!NOTE]
>In javascript is exponent.  It raised the number to its power. (eg. 5 **2 -> 25 ).  Also there is other method named “Math.pow(5,2)” which returns the same 25 value.

**Comparison operators:**
		“===” or “!==” are strict versions of comparison operators.  It is always best to use them.  Because, they used to compare both data and datatype.  The normal “==” or “!=” compares only the data.

## String in Javascript

Strings enclosed within backticks (\`) are called template litereals.  As the name itself describes that, we can include variable names inside the string.  (eg. “hi, my name is ${name}.”).
We can also include expression in template literals. (eg. \`The value of 20/5 is ${20/5}.\`).

### Common string methods:

Includes() method take one input parameter and check’s whether the given input string is present in the original string as a substring or not.  (eg. “googlechrome” -> str.includes(“chrome”) returns true, since it is present in the string”.)

To find the position of substring use the indexof() method which takes to two input parameters. It returns the start index of the substring if found, else it will return -1 as return number.  For more  information, refer mdn docs. Note: the indexof() method has two input parameters, one is the string and the other is the index number, from where the search should start from.  If the second parameters is omitted it’ll start the search from the first index.

Slice(): The slice() method returns the substring from the string.  It takes two input parameters one is the start index and the other is end index.  If the second parameter is not provided it’ll return the remaining characters from the string.

Replace(): The replace() method replace the substring with new substring. (eg. “mozilla” , str.replace(“moz”,”van”), “vanilla”).  Also refere replaceall in mdn docs (it replaces all the occurrence of the substring.)


## Arrays in javascript:

NOTE: YOU CAN DECLARE ARRAY TYPE AS CONSTANT AND MAKE MODIFICATIONS. IT’LL WORK, BECAUSE THAT VARIABLE IS ONLY POINTING TO THE OBJECT LOCATION.  
Index() method in array like we have for string.  We pass the input value to find the index position of that value in the array.

### Adding items to the array

Push() – to add new items to the end of the array. It returns the new length of array which can be stored in a variable if required.

Unshift() – to add new items to the start of the array.

### Removing items from the array

Pop() – to remove the last item from the array.  It also returns the removed item from the array incase if we want to store it.

Shift() – to remove the first item from the array.

Splice() – if we know the index of the element we can remove the item by specifying the index directly.  This method takes two input parameters, one is index and the other number of items to remove.

### Loops for arrays

Map() -> takes a callback function as an argument and executes for every item in the array

For eg.
const numbers=[2,3,4,5];
Const newNumbers=numbers.map((n)=>{ return n*2}};
It returns every number present in the numbers array multiplied by 2 and stores it in the newNumbers array.

Filter() – The filter() is useful if you want filter array based on certain conditions. (eg. Where you want to store the elements of the array, if the element length is only greater than 8 ).  For more info, refer mdn docs.

## Functions in javascript

**btn.addEventListener('click',displayMessage);**

You might be wondering why we haven't included the parantheses after the function name.  This is because we don't want to call the function immediately - only after the button has been clicked.  If you try changing the line to

**btn.addEventListener('click',displayMessage());**

and saving and realoading, you'll see that the message box appears without the button being clicked!  The parantheses in this context are sometimes called the "function invocation operator".  You only use them when you want to run the function immediately in the current scope.  In the same respect, the code inside the anonymous function is not run immediately, as it is inside the function scope.

## Classes in Javascript
Classes are a template for creating objects.  They encapsulate data with code to work on that data.  Classes in javascript are built on prototypes but also have some syntax and semantics.  They are similar to classes in other object-oriented programming languages such Java and C++.

>Private fields in Javascript can also be created using the hash (#) prefix before the field name.  This makes the field truly private and inaccessible from outside the class.

## public fields in javascript
Private fields also have their public counterparts, which allow every instance to have a property. Fields are usually designed to be independent of the constructor's parameters. For example:
Public fields are almost equivalent to assigning a property to this. For example, the above example can also be converted to:
```Javascript
class MyClass {
  constructor() {
    this.luckyNumber = Math.random();
  }
}
```
## Diamond problem in Javascript
The diamond problem is a common issue in multiple inheritance scenarios where a class inherits from two classes that both inherit from a common superclass. This can lead to ambiguity about which inherited properties or methods should be used.

[Click here to know more about diamond problem in Javascript.](https://en.wikipedia.org/wiki/Multiple_inheritance#The_diamond_problem)

## promises in javascript
A Promise is an object representing the eventual completion or failure of an asynchronous operation. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason.

A Promise is in one of these states:
- Pending: Initial state, neither fulfilled nor rejected.
- Fulfilled: The operation completed successfully.
- Rejected: The operation failed.

## async and await in javascript
The async function declaration defines an asynchronous function, which returns an AsyncFunction object. An async function is a function that is declared with the async keyword, and the await keyword is permitted within it.
The await operator is used to wait for a Promise. It can only be used inside an async function. The await expression causes async function execution to pause until a Promise is settled (that is, fulfilled or rejected), and to resume execution of the async function after fulfillment. When resumed, the value of the await expression is that of the fulfilled Promise.

Example:
```Javascript
async function fetchData() {
  try {
    let response = await fetch('https://api.example.com/data');
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error fetching data:', error);
  }
}
```
In this example, the fetchData function is declared as async, allowing the use of await to pause execution until the fetch operation and subsequent JSON parsing are complete.

## promise chaining in javascript
Promise chaining is a technique that allows you to chain multiple asynchronous operations together. Each operation returns a Promise, and the next operation in the chain waits for the previous one to complete before executing.

Example:
```Javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log(data);
    return fetch('https://api.example.com/other-data');
  })
  .then(response => response.json())
  .then(otherData => {
    console.log(otherData);
  })
  .catch(error => {
    console.error('Error:', error);
  });
```
[Refer here for more information on promise chaining in Javascript.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises#chaining)

## composition in promises

There are four composition tools for running asynchronous operations concurrently: Promise.all(), Promise.allSettled(), Promise.any(), and Promise.race().

**All()** - The promises settles when all the promises are completed.
**allSettled()** - This returned promise fulfills when all of the input's promises settle (including when an empty iterable is passed), with an array of objects that describe the outcome of each promise.
**Any()** - This promise settles when any one of the promise gets completed.
**Race()** - The promises settles when the promise passed in the array which gets completed first.