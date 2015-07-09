JavaScript questions
====================

What will be logged for this functions?

**First function**
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

First log:
```
Kyle
```

Second log:

```
Kyle
```
**Fourth function**
```
var foo = "Bazinga";

function myFunction() {
	var foo = "Kyle";
}

myFunction();
console.log(foo);

```

*Answer:*

First log:
```
Kyle
```

Second log:
```
Bazinga
```

**Fifth function**
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
Bazinga
```
