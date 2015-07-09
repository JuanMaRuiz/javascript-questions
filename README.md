JavaScript questions
====================

What will be logged for this functions?

```
foo();
function foo() {
	console.log("Bazinga");
}
```
Answer: 

```
Bazinga
```

```
foo();
var foo = function(){
	console.log("Bazinga");
}
```

Answer: 

```
Error foo is not a function
```

```
var bar = "John Doe";

if(true){
	var bar = "Kyle";
	console.log(bar);
}

console.log(bar);

```

Answer: 

First log:
```
Kyle
```

Second log:

```
Kyle
```

```
var foo = "Bazinga";

function myFunction() {
	var foo = "Kyle";
}

myFunction();
console.log(foo);

```

Answer:

First log:
```
Kyle
```

Second log:
```
Bazinga
```


```
var foo = "Bazinga";

function myFunction() {
	foo = "Kyle";
}

myFunction();
console.log(foo);
```

Answer: 

```
Bazinga
```
