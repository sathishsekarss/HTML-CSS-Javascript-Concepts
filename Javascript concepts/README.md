Table of contents
1. [Variable declaration](#variable-declaration)
2. [Number objects](#number-objects)
3. [String in Javascript](#string-in-javascript)
	3.1. [Common string methods](#common-string-methods)

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


