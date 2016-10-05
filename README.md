JavaScript questions
====================

***What will be logged for this functions?

 **First function**

> ```
> var foo = "Bazinga";
>
> function myFunction() {
> 	foo = "Kyle";
> }
>
> myFunction();
> console.log(foo);
> ```

> *Answer:*
	```
	Kyle
	```

**Second function**
> ```
> foo();
> var foo = function(){
> 	console.log("Bazinga");
> }
> ```

> *Answer:*
  ```
  Error foo is not a function
  ```
  _Variables are always moved (‘hoisted’) to the top of their JavaScript scope. ```foo``` is moved to the top but not the function._

**Third function**
> ```
> var bar = "John Doe";
>
> if(true){
> 	var bar = "Kyle";
> 	console.log(bar);
> }
>
> console.log(bar);
>
> ```

> *Answer:*

  * First log:
  ```
  Kyle
  ```

  * Second log:
  ```
  Kyle
  ```
  **Why?**
  _```if``` statements doesn't create his own scope_

**Fourth function**
> ```
> var foo = "Bazinga";
>
> function myFunction() {
> 	var foo = "Kyle";
> 	console.log(foo);
> }
>
> myFunction();
> console.log(foo);
>
> ```

> *Answer:*

* First log:
    ```
    Kyle
    ```

    * Second log:
    ```
    Bazinga
    ```

**Fifth function**
> ```
> foo();
> function foo() {
> 	console.log("Bazinga");
> }
> ```

>*Answer:*

  ```
  Bazinga
  ```

  **Why?**
  _Function declarations and function variables are always moved (‘hoisted’) to the top of their JavaScript scope._

**Sixth function**
> ```
> var foo = "Bazinga";
>
> function bar() {
> 	var foo = "bb-8";
>
> 	function baz(foo){
> 		foo = "R2D2";
> 		bam = "C3PO";
> 	}
>
> 	baz();
> }
>
> bar();
> foo;
> bam;
> baz();
> ```

> *Answer:*

  ```
  "Bazinga"
  "C3PO"
  ReferenceError
  ```

  **Why?**
  _foo variable in baz function doesn't change the value of the global variable because in this function there si a reference in his own scope to a foo variable (passed as an argument). The second log ```bam``` log the value created in baz function because there is no reference inside the function. So JS create an global variable with that value. When you execute baz you get an error because baz is defined inside the bar function scope, so there's no function in the global scope you can call._

**Seventh function**
> ```
> var foo = function bar() {
> 	var foo = "Bazinga";
>
> 	function baz(foo){
> 		foo = bar;
> 		foo;
> 	}
> 	baz();
> };
>
> foo();
> bar();
>
> ```

> *Answer:*
  ```
  Error!
  ```
  **Why?**
  _bar function is assigned to foo var. If you want to call bar function you must to do invoking foo as a function_

**Eighth function**
> ```
> var foo = "R2D2";
>
> function bar() {
> 	foo = "C3PO";
> 	var foo;
> }
>
> bar();
> console.log(foo);
> ```

> *Answer:*
  ```
  R2D2
  ```
  **Why?**
  _First you declare a variable in the global scope. Inside bar function you set the value to local foo var to C3PO. Inside bar function var foo is hoisting to the top of his scope (bar function) so
  this value has no effect over global variable foo_

  **Ninth function**
> ```
> function foo(2,3);
>
> function foo(a,b) {
>   return a + b;
> }
>
> bar(1,2);
>
> var bar = function(x,y) {
> return x * y;
> }

> *Answer:*
 ```
 5
 ReferenceError: Can't find variable bar
 ```
 **Why?**
 _If a function is defined using a function declaration ```foo()```, the whole function is hoisted to the top of the function, meaning that it can be invoked before it has been defined.
>  A function expression ```bar()``` (where an anonymous function is assigned to a variable) is hoisted in a similar way to variables. So the declaration will be hoisted, but not the actual function_

##More questions

* [5 Typical JavaScript Interview Exercises](http://www.sitepoint.com/5-typical-javascript-interview-exercises/)
* [5 More JavaScript Interview Exercises](http://www.sitepoint.com/5-javascript-interview-exercises/)
* [JS: Interview Algorithm - Begginer](http://thatjsdude.com/interview/js1.html)
* [JS: Basics and Tricky Questions - Intermediate](http://thatjsdude.com/interview/js2.html)