# Javascript

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8"/>
    </head>
    <body>
        <script type="text/javascript">
            alert('Hello world');
        </script>
    </body>
</html>
```

* MAC chrome developer mode : cmd+alt+j

* numbers auto cast
```javascript
alert(1+1.0);	// 2
alert(Math.pow(3,2));	// 9

alert(typeof “1”);	// string
alert(typeof 1);	// number 
alert(‘shaun\’s javascript’);	// shaun’s javascript
alert("coding"+" everybody");	// coding everybody
alert("coding everybody".length);	// 16
```

* declaration
```javascript
var a = 1; var b;
```

* assign operator
=

* equal operator 
== 
```javascript
alert(1 == “1”);	// true
```

* strict equal operator
===
```javascript
alert(1 === “1”);	// false
```

* undefined: not intended  none value. undefined is a datatype
* null : intended none value. null is a datatype
```javascript
alert(null == undefined);       //true
alert(null === undefined);      //false
alert(true == 1);               //true
alert(true === 1);              //false
alert(true == '1');             //true
alert(true === '1');            //false
 
alert(0 === -0);                //true
alert(NaN === NaN);             //false
```

* not equal
!=

* strictly not equal
!==

* conditional statement
```javascript
if (false){
	alert(1);
} else if (true) {
	alert(2);
} else if (true) {
	alert(3);
} else {
	alert(4);
}   // 2 —>  3 이전에 조건 만족했으므로 3까지 안감
```

* get user input
```javascript
prompt(‘your age?’); 
alert(prompt(‘your age?’)); // 20
```

* Logic operator 
&&
||

* can use more than 2
```javascript
if (true && true && false || true){
	statement
}
```

* empty string, null, undefined treat as false, else true
```javascript
if (''){} // false
```

* 0 treat as false, else true
```javascript
if(0){
	alert("false");
}else if(-1){
	alert("true");
}
```

* while
```javascript
while( condition ){

}
```

* While loop control
```javascript
break; // === out of loop
continue; // === skip and continue loop
```

---
* Using chrome debugger : cmd + alt + j
1. Set break pt
2. Step into next function call: goes into function
	* global show every results
	* Watch Expressions: i --> show only what we want

---

* Function: Allow a logic re-usable
```javascript
function name( [arg...[,arg]]){
	code
	return value
}

```

