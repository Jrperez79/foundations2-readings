# Reading-01

## Template Literals
Template literals are string literals allowing embedded expressions. You can use multi-line strings and string interpolation features with them.

### Syntax
    - `string text`
    - `string text line 1 string text line 2`
    - `string text ${expression} string text`
    - tag`string text ${expression} string text`

Template literals are enclosed by the backtick (` `) (grave accent) character instead of double or single quotes.

## Getting Literal with ES6 Template Strings
Template Strings fundamentally changed the limited capabilities of strings in JavaScript.

String Substitution 
Substitution allows us to take any valid JavaScript expression (including say, the addition of variables) and inside a Template Literal, the result will be output as part of the same string.

Template Strings significantly simplify multiline strings.
Example: 
console.log(`string text line 1
string text line 2`);
Outputs: 
string text line 1
string text line 2

## CSS-Tricks Template Literals
The Template Literal, introduced in ES6, is a new way to create a string. With it comes new features that allow us more control over dynamic strings in our programs.

Expressions
Example: ${expression};

HTML Templates
With the ability to have multi-line strings and use Template Expressions to add content into our string, this makes it really nice to use for HTML templates in our code.

## Array.forEach Method
The forEach() method executes a provided function once for each array element.

Syntax
    - Callback
        - Function to execute on each element. It accepts between one and three arguments.
    - currentValue
        - The current element being processed in the array.
    - index 
        - The current value in the array.
    - thisArg 
        - Value to use as this wen executing callback.

forEach() calls a provided callback function once for each element in an array in ascending order. It is not invoked for index properties that have been deleted or are uninitialized. 

callback is involved with three arguments:
    - the value of the element
    - the index of the element
    - the Array object being traversed

forEach() executes the callback function once for each array element; unlike map() or reduce() it always returns the value undefined and is not chainable. The typical use case is to execute side effects at the end of a chain.

forEach() does not mutate the array on which it is called. (However, callback may do so)

Examples:
No operation for uninitialized values (sparse arrays)
Converting a for loop to forEach
Printing the contents of an array
Using thisArg - updates an object's properties from each entry in the array
An object copy function - creates a copy of a given object
Modifying the array during iteration - When the entry containing the value two is reached, the first entry of the whole array is shifted off—resulting in all remaining entries moving up one position. Because element four is now at an earlier position in the array, three will be skipped.
Flatten an array - If you want to flatten an array using built-in methods you can use Array.prototype.flat()

## For loops vs forEach in JavaScript
The for loop is likely the first type of loop you learned about when you were learning JavaScript.
forEach is a method on the Array prototype.
 Example:   
 students.forEach(function(student) {
  console.log(student);
}); 

###When to use a for loop over forEach
forEach comes with a little caveat. It only works on arrays. So if you want to actually count, forEach probably isn’t your friend

Use lodash. I use lodash in almost all my projects. In case you don’t know what lodash is, it’s basically a utility library in JavaScript that lets you do a lot of common things. lodash has a lot of helpful iteration methods, such as forEach and map. 
Create a helper function. lodash actually uses a while loop under the covers.

Since forEach is pretty idiomatic in many languages, it becomes extremely explicit what you’re doing when you use a forEach method. Regular for loops are not bad, I just think forEach reads better and makes it simpler to reason about.




