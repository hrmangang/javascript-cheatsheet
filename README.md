## JavaScript CheatSheet by Ronald Mangang

### Basics

```js
<script language="javascript" type="text/javascript">
  // javascript code.
  document.write("This is how you can write text");
</script>
  ```

/* not really necessary to write language and type above.
   semi-colons are optional but are a good practice.
   javascipt is case-sensitive.
*/

Henceforth, the <script> tags are omitted.

### Variables & data types

```js
  var num; // declaration
  num = 5; // assignment
  typeof(num) // returns its datatype
```

/* variables have to be declared before used, but can hold
   any data type, such as numbers, strings, booleans, etc.
*/
  
Variables can be local or global. Local variables override global variables with the same name.

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
```

```js
  // comparison
  var a = 50, b = 100;
  a == b; // equal
  a != b; // not equal
  a > b; // greater than
  a < b; // less than
  a >= b; // greater than or equal to
  a <= b; // less than or equal to
```

```js
  // logical
  var a = 1, b = 0;
  a && b; // logical AND
  a || b; // logical OR
  !a; // logical NOT
  ```

```js
  bitwise
  var a = 5, b = 7;
  a & b; // bitwise AND
  a | b; // bitwise OR
  a ^ b; // bitwise XOR
  ~a; // bitwise NOT
  a << 1; // left shift
  a >> 1; // right shift
  a >>> 1; // right shift with zero
  ```

```js
  // assignment
  var a = 5;
  a += 5; // add and assign
  a -= 5; // subtract and assign
  a *= 5; // multiply and assign
  a /= 5; // divide and assign
  a %= 5; // modulus and assign
  // the same logic applies to bitwise operators as well.
  ```

```js
  // conditional
  var x = (condition) ? this_value_if_true : else_this_value ;

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

  for (init, test, update) {
    do_this;
  }

  for (x in object) {
    do_this; // repeat for each element/property in the object
  }
  ```

  loop control
```js
  break;
  continue;
  ```
  
  
  
