## JavaScript CheatSheet by Ronald Mangang

### Basics

```js
<script language="javascript" type="text/javascript>
  // javascript code.
  document.write("This is how you can write text");
</script>
```

/* not really necessary to write language and type above.
   semi-colons are optional but are a good practice.
   javascipt is case-sensitive.
*/

// VARIABLES & DATA-TYPES

<script>
  var num; // declaration
  num = 5; // assignment
</script>

/* variables have to be declared before used, but can hold
   any data type, such as numbers, strings, booleans, etc.
*/

<script>
  var num = 5;
  typeof(num); // to see its datatype
</script>

/* variables can be global or local.
   local variables override global variables with the same name.
*/

// OPERATORS

// arithmetic
<script>
  var a = 50, b = 100;
  a + b; // addition
  a - b; // subtraction
  a * b; // multiplication
  a / b; // division
  a % b; // modulus
  a++;  // increment
  b++;  // decrement
</script>

// comparison
<script>
  var a = 50, b = 100;
  a == b; // equal
  a != b; // not equal
  a > b; // greater than
  a < b; // less than
  a >= b; // greater than or equal to
  a <= b; // less than or equal to
</script>

// logical
<script>
  var a = 1, b = 0;
  a && b; // logical AND
  a || b; // logical OR
  !a; // logical NOT
</script>

// bitwise
<script>
  var a = 5, b = 7;
  a & b; // bitwise AND
  a | b; // bitwise OR
  a ^ b; // bitwise XOR
  ~a; // bitwise NOT
  a << 1; // left shift
  a >> 1; // right shift
  a >>> 1; // right shift with zero
</script>

// assignment
<script>
  var a = 5;
  a += 5; // add and assign
  a -= 5; // subtract and assign
  a *= 5; // multiply and assign
  a /= 5; // divide and assign
  a %= 5; // modulus and assign
  // the same logic applies to bitwise operators as well.
</script>

// conditional
<script>
  var x = (condition) ? this_value_if_true : else_this_value ;
</script>

// FLOW OF CONTROL (almost copy-paste from C/C++ syntax)

// if, if else, if else if constructs
<script>
  
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

</script>

// switch statements
<script>
  
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

</script>

// loops
<script>
  
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

</script>

// loop control
<script>

  break;
  continue;
  
</script>
