## JavaScript CheatSheet

Compiled and edited by Ronald Mangang.
Hope it helps anyone looking for a JS cheatsheet.

(it's still under development)

### Basics

```
<script language="javascript" type="text/javascript">
  // javascript code.
  document.write("This is how you can write text");
</script>
  ```
It is not necessary to write **language** and **type** as given above. Also, semi-colons are optional but are a good practice.

Henceforth, the script tags will be omitted.

### Variables & data types

```js
  var num; // declaration
  num = 5; // assignment
  typeof(num) // returns its datatype
```
Variables have to be declared before used, but can hold any data type, such as numbers, strings, booleans, etc. They can be local or global. Local variables override global variables with the same name.

### Operators

```js
  // arithmetic
  var a = 50, b = 100;
  a + b; // addition
  a - b; // subtraction
  a * b; // multiplication
  a / b; // division
  a % b; // modulus
  a++;  // increment
  b++;  // decrement

  // comparison
  var a = 50, b = 100;
  a == b; // equal
  a != b; // not equal
  a > b; // greater than
  a < b; // less than
  a >= b; // greater than or equal to
  a <= b; // less than or equal to
        
  // logical
  var a = 1, b = 0;
  a && b; // logical AND
  a || b; // logical OR
  !a; // logical NOT
  
  // bitwise
  var a = 5, b = 7;
  a & b; // bitwise AND
  a | b; // bitwise OR
  a ^ b; // bitwise XOR
  ~a; // bitwise NOT
  a << 1; // left shift
  a >> 1; // right shift
  a >>> 1; // right shift with zero
  
  // assignment
  var a = 5;
  a += 5; // add and assign
  a -= 5; // subtract and assign
  a *= 5; // multiply and assign
  a /= 5; // divide and assign
  a %= 5; // modulus and assign
  // the same logic applies to bitwise operators as well.
  
  // conditional
  var x = (condition) ? this_value_if_true : else_this_value ;
  ```

### Flow of control
  (almost copy-paste from C/C++ syntax)

  if, if else, if else if constructs
  
```js
  if (condition) {
    do_this;
  }

  if (condition) {
    do_this;
  } else {
    do_this;
  }

  if (condition) {
    do_this;
  } else if (condition) {
    do_this;
  } else {
    do_this;
  }
  ```

  switch statements
```js
  switch (expression) {
    case value_1:
      do_this;
      break;
    case value_2:
      do_this;
      break;
    default:
      do_this;
  }
  ```

  loops
```js
  while (condition) {
    do_this;
  }

  do {
    do_this;
  } while (condition);

  for (init; condition; update) {
    do_this;
  }

  for (x in object) {
    do_this; // repeat for each element/property in the object
  }
  ```

  loop control
```js
  break; // terminate the current loop
  continue; // skip to the next iteration
  
  // one can also use labels
  
  outer: // a label
  for (var i = 0; i < 10; i++) {
    do_this;
    inner: // another label
    for (var j = 0; j < 10; j++) {
      do_this;
      if (condition) break inner; // same as break;
      if (condition) break outer;
      if (condition) continue inner; // same as continue;
      if (condition) continue outer;
      }
  }
  ```
  
### Functions
  
```js
  function fname(parameters) {
    do_this;
    return value;
  }
  ```
  
In HTML, the above function can be called as
```html
  <input type="button" onclick="fname(arguments);" value="Click here">
  ```

The above code generates a button whose value is "Click here". When clicked, the function "fname" is invoked.
  
Functions can also be dynamically defined using **Function()** constructor along with **new** operator. It accepts string parameters and the last parameter is the body of the function.
```js
  var fname = new Function("x", "y", "return x*y"); // note the use of string parameters and function body
  ```
  
An unnamed function can be defined using **function literals** (given below). Function literals are cool because they are used as expressions rather than as statements.
```js
  var fname = function(parameters) {
                do_this;
              };
  ```
  
1. Function defintions can be nested inside other functions. But they can't be put within loops or conditionals.
2. Function literals, however, can appear within any JavaScript expression.

### Redirection
  
(yeah that annoying feature!)
  
The following line puts a link named "Refresh" and when clicked, it refreshes the current page.
  
```html
  <a href="javascript:location.reload(true)">Refresh</a>
  ```
  
For an auto refresh after 10 seconds (say), use the following function.
```js
  setTimeout("location.reload(true);", 10); 
  ```
  
To redirect to some URL, use the following function.
```js
  window.location = "https://github.com/ronaldmangang"';
  ```
### Dialog box
  
Dialog boxes can be displayed in events. There are three main types.  
  
```js
  // alert dialog box
  alert("Warning!"); // displays the text
  
  // prompt dialog box
  var val = prompt("Enter name: ", "your name here"); // the first parameter is the label, the second parameter is the default string to be displayed in the text box
  // val will hold the string entered by the user.
  
  // confirmation dialog box
  var val = confirm("Are you sure?"); // returns true if user clicks OK, false otherwise
  ```
  
### Objects
  
The **new** operator followed by a constructor method is used to create objects.
  
```js
  var person = new Object();
  person.name = "Einstein"; // defining properties (attributes) of the object
  person.field = "Physics";
  ```

The keyword **this** is used to refer to the object that has been passed to a function.
  
```js
  function updateAge(age) {
    this.age = age;
  }
  
  function person(name, field) {
    this.name = name;
    this.field = field;
    this.updateAge = updateAge; // defining methods
  }
  
  var obj = new person("Einstein", "Physics"); // person() becomes a constructor
  obj.updateAge(50); // age = 50
  ```
  
Put the object as an argument to **with** and refer to its attributes without the object's name and dot.
  
  ```js
  function student(points);
    with (this) {
      marks = points; // same as this.marks = points
    }
  }
  ```
  
### Arrays
  
Array methods
```js
  arr_1.concat(arr_2, arr_3) // returns concatenated array of arr_1, arr_2 and arr_3
  ```
  
TO BE WRITTEN LATER...
  
### Exception handling
  
```js
  try {
    // try_running_this_code;
  } catch (e) {
    // do_this_if_exception_occurs;
    document.write(e.description) // writes the description of the exception occured
  } finally { // optional
    // do_this_regardless_of_exception_occuring;
  }
  ```
  
To raise exceptions (both built-in and user-defined), use **throw** statement. Try putting throw statement anywhere inside the try block (maybe inside a function).
  
```js
  try {
    if (condition) {
      throw("some funny error");
    } else {
      do_this;
    }
  } catch (e) {
    document.write(e)
  }
  ```
  
### Animation

```js
  setTimeout(function, t); // calls function after t milliseconds from now
  setInterval(function, t); // calls function after every t milliseconds
  clearTimeout(setTimeout_variable); // clears any timer set by setTimeout()
  
  // set the position of a DOM object anywhere on the screen
  object.style.left = d; // set distance (d) in pixels or points from left edge of the screen
  object.style.top = d; // set distance (d) in pixes or points from top edge of the screen
  ```
 
The following is a code that changes a picture to another when mouse hovers over it and then changes back to original image when mouse moves away from it.

```js
  if (document.images) { // check if images are present
    var img_1 = new Image();
    img_1.src = "/images/original.gif";
    var img_2 = new Image();
    img_2.src = "/images/new.gif";
  }
  ```
In the HTML, write

```html
  <a href="#" onMouseOver="document.theImage.src=img_2.src;"
              onMouseOut="document.theImage.src=img_1.src;">
    <img name="theImage" src="images/original.gif" </img></a>
  ```
  

  
  





