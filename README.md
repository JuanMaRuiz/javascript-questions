JavaScript questions
====================

What will be logged for this functions?

**First function**

```
var foo = "Bazinga";

function myFunction() {
	foo = "Kyle";
}

myFunction();
console.log(foo);
```

*Answer:*

```
Kyle
```

**Second function**
```
foo();
var foo = function(){
	console.log("Bazinga");
}
```

*Answer:*

```
Error foo is not a function
```
_Variables are always moved (‘hoisted’) to the top of their JavaScript scope. ```foo``` is moved to the top but not the function._

**Third function**
```
var bar = "John Doe";

if(true){
	var bar = "Kyle";
	console.log(bar);
}

console.log(bar);

```

*Answer:*

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
```
var foo = "Bazinga";

function myFunction() {
	var foo = "Kyle";
	console.log(foo);
}

myFunction();
console.log(foo);

```

*Answer:*

* First log:
```
Kyle
```

* Second log:
```
Bazinga
```

**Fifth function**
```
foo();
function foo() {
	console.log("Bazinga");
}
```
*Answer:*

```
Bazinga
```

**Why?**
_Function declarations and function variables are always moved (‘hoisted’) to the top of their JavaScript scope._

**Sixth function**
```
var foo = "Bazinga";

function bar() {
	var foo = "bb-8";

	function baz(foo){
		foo = "R2D2";
		bam = "C3PO";
	}

	baz();
}

bar();
foo;
bam;
baz();
```
*Answer:*

```
"Bazinga"
"C3PO"
ReferenceError
```

**Why?**
_foo variable in baz function doesn't change the value of the global variable because in this function there si a reference in his own scope to a foo variable (passed as an argument). The second log ```bam``` log the value created in baz function because there is no reference inside the function. So JS create an global variable with that value. When you execute baz you get an error because baz is defined inside the bar function scope, so there's no function in the global scope you can call._

##More questions

* [5 Typical JavaScript Interview Exercises](http://www.sitepoint.com/5-typical-javascript-interview-exercises/)
* [5 More JavaScript Interview Exercises](http://www.sitepoint.com/5-javascript-interview-exercises/)
* [JS: Interview Algorithm - Begginer](http://thatjsdude.com/interview/js1.html)
* [JS: Basics and Tricky Questions - Intermediate](http://thatjsdude.com/interview/js2.html)