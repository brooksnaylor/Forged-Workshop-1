# Forged Workshop 1


#### Numbers

1. Enter the following expressions into your console.

   ```js
   1 + 2
   3 * 5
   5 / 4 - 13
   5000 * 234
   1073 / 57 + 200
   ```

2. Why are the values produced by the following two expressions different? What
   are they?

   ```js
   3 + 2 * 4 - 1;        // => 10
   (3 + 2) * (4 - 1);    // => 15
   ```

   **ANSWER**: The first expression evaluates to 10 and the second expression evaluates to 15. The addition of parentheses in the second example to wrap `(3 + 2)` and `(4 - 1)` changes the order in which the code is evaluated. This is because JavaScript evaluates mathematical expressions according to an order of operations, just like in mathematics. The order is PEMDAS (Parentheses, Exponents, Multiplication, Division, Addition, Subtraction).

3. Calculate how old you are in minutes using the console.

   ```js
   // If you are 30 years old:
   30 * 365 * 24 * 60;     // => 15768000
   ```

4. What is the percentage of people in the class with brown hair? Use the
   console to find out.

   ```js
   12 / 15 * 100;     // => 80
   ```

5. Try the following expressions in the console:

   ```js
   6 % 2
   42 % 10
   5 % 2
   6 % 3
   7 % 4
   100 % 12
   ```

   What is the significance of the result? How does the `%` (modulus) operator
   work?

   **ANSWER**: The modulo operator works by dividing the first operand (the one to the left of the %) by the second operand (the  one to the right of the %) and returning the remainder of that division.

6. Try the following:

   ```js
   3 % 2
   4 % 2
   5 % 2
   6 % 2
   ```

   What do the results tell you about the first operand to the modulus operator?

   **ANSWER**: The first operand is the number being divided.

#### Strings

1. Write a string that represents your full name.

   ```js
   'Ernest Hemingway';
   ```

2. Write a string that represents your favorite food.

   ```js
   'Steak';
   ```

3. Use the `+` operator to combine (known as *concatenation*) two or more
   strings, *e.g.*:

   ```js
   // Your first and last names
   "John" + " " + "Doe"
   ```

   + Your first and last names (as shown above)
      ```js
      "Ernest" + " " + "Hemingway";
      ```
   + Your parents' full names
      ```js
      "Clarence Hemingway" + " " + "Grace Hemingway";
      ```
   + Your home town and state
      ```js
      "Oak Park" + ", " + "Illinois";
      ```

4. Fix the errors in the following strings:

   ```js
   Where are all the quotes?
   'hmm something is not right"
   'Do other ' * 'operators work with string concatenation?
   ```

   **FIXED**:
   ```js
   "Where are all the quotes?";
   "hmm something is not right";
   'Do other ' + 'operators work with string concatenation?';
   ```
   
### Functions

#### Basic Practice (5 points each)

1. In your console, copy the following function and verify
   that the following invocations match your expectations:

   ```js
   function square(num){
      return num * num;
   }

   square(10) + 2;
   square(100) + square(77);
   square(8 / 2)
   square(2 + 17);
   square(square(15));
   ```

2. Write a sentence in plain English describing how `square(square(15))` is
   evaluated.

   **ANSWER**: The inner function call `square(15)` is evaluated first, then its result is used to evaluate the outer function call.

3. Rename `square`'s `num` parameter in your above code to `monkey`, and
   rename the uses of that parameter in the body to `monkey` as well. Will the
   function `square` still work? Why or why not?

   **ANSWER**: The function `square` will still work, because the parameter `monkey` simply represents a placeholder for an actual value that is provided when the function is called. Thus, it does not need to be named semantically for the code to work.

4. What is wrong with the following definitions of `square`? Write a sentence or
   two describing the issue(s); then, try copying the erroneous examples into a
   console one-at-a-time and observing the error(s) generated (you may have to
   attempt to invoke the functions to see the error). What errors are produced
   (if any) for each erroneous version? Do the errors make sense?

   ```js
   function square(monkey) {
     return x * x;
   }
   ```

   **PROBLEM**: There is no reference to x available. The parameter `monkey` should be refactored to `x` or vice versa for the function to work.

   ```js
   function square(5) {
     return 5 * 5;
   }
   ```

   **PROBLEM**: The number 5 cannot be used as a function parameter. Parameters must be placeholders/labels, not actual values.

   ```js
   function square("x") {
     return "x" * "x";
   }
   ```

   **PROBLEM**: Similar to above, the string `"x"` cannot be used as a function parameter. Parameters must be placeholders/labels, not actual values. Also, strings cannot be multiplied together. The parameter should be refactored to `x` and the body of the function should be refactored to: `return x * x;`

5. Fix the invalid syntax in the following functions (you can copy and paste these
   invalid definitions into your console and then edit them there):

   ```js
   func square1(x {
     return x * x;
   }

   functionsquare2 x)
     return x * x;
   }

   function (x) square3 {
     return x * x;
   ```

   **FIXED**:
   ```js
   function square1(x) {
     return x * x;
   }

   function square2(x) {
     return x * x;
   }

   function square3(x) {
     return x * x;
   }

6. The following functions exhibit poor style -- fix these issues using the
   original version of `square` as a reference.

   ```js
   function square(x){return x*x;}

   function square (x) { return x *x;
   }

   function square(x)
   {
   return x * x;
   }
   ```

   **FIXED**:
   ```js
   function square(x) {
      return x * x;
   }

   function square(x) {
      return x * x;
   }

   function square(x) {
      return x * x;
   }
   ```

7. Complete the function `cube` that returns the cube of x:

  ```js
  function cube(x) {
    // your code here
  }
  ```

  **ANSWER**:
  ```js
  function cube(x) {
    return x * x * x;
  }

  // OR

  function cube(x) {
    return Math.pow(x, 3);
  }
  ```

8. Complete the function `fullName` that should take two parameters, `firstName`
   and `lastName`, and returns the `firstName` and `lastName` concatenated
   together with a space in between.

   ```js
   // don't forget the parameters!
   function fullName() {
    // your code here
   }
   fullName("John", "Doe") // => "John Doe"
   ```

   **ANSWER**:
   ```js
   function fullName(firstName, lastName) {
      return firstName + " " + lastName;
   }
   ```

9. Write a function `average` that takes two numbers as input (parameters), and
   returns the average of those numbers.

   **ANSWER**:
   ```js
   function average(num1, num2) {
      return (num1 + num2) / 2;
   }

10. Write a function `greeter` that takes a name as an argument and *greets*
    that name by returning something along the lines of `"Hello, <name>!"`

  **ANSWER**:
   ```js
   function greeter(name) {
      return "Hello, " + name + "!";
   }
   ```

11. Using the document found at <a href="http://www.gbcnv.edu/documents/ASC/docs/00000005.pdf" target="_blank">this link</a>, translate the first page of geometric
    formulas into JavaScript functions.

    **ANSWER**: As an example, a function to compute the perimeter of a rectangle might look
    like this:

    ```js
    function perimeterRect(l, w) {
      return 2 * (l + w);
    }
    ```

    **NOTE:** JavaScript provides some nifty mathematical functions and
    constants built into the language that you'll need for this exercise. The
    two that we'll be making use of are:

    ```js
    Math.PI; // => 3.141592653589793
    Math.sqrt(256); // => 16
    ```

    To test your answers, you'll need to:

    1. Code your function in the console in the way that you think it will work
    2. Call the function with arguments in the console to see the result, e.g.
      `perimeterRect(2, 6)`.
    3. Eventually, you may want to verify that the output is correct. Google is a
       great tool for this:


![google geometry answer](google-geometry-answer.gif)
