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



##More questions

* [5 Typical JavaScript Interview Exercises](http://www.sitepoint.com/5-typical-javascript-interview-exercises/)
* [5 More JavaScript Interview Exercises](http://www.sitepoint.com/5-javascript-interview-exercises/)
* [JS: Interview Algorithm - Begginer](http://thatjsdude.com/interview/js1.html)
* [JS: Basics and Tricky Questions - Intermediate](http://thatjsdude.com/interview/js2.html)