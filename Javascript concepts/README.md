Table of contents
1. [Variable declaration](#variable-declaration)
2. [Number objects](#number-objects)

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
