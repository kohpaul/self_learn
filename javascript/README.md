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
	1. re-usability
	2. maintenance
	3. readability


* input : arg inside ( )
```javascript
function get_argument(arg1, arg2){
	return arg1 + arg2;
} // can have multiple parameters(args) but can only return one output

alert(get_argument(1, 2));
```

* Multiple ways to declare function <br>
below is same as above
```javascript
	get_argument = function(arg1, arg2){
		return arg1 + arg2;
	}
```

* Anonymous function: used for one time use: Using it as it declares the function
```javascript
(function (){
	return 1;
})();
```

* Array: allow return multiple elements
```javascript
var arr = ['asd', 'zxc', 'qwe'];
alert(arr); // add,xxc,qwe
alert(arr[0]); // asd
alert(arr.length); // 3
alert(arr[1].toUpperCase()); // ZXC
```

```javascript
var li = ['a', 'b', 'c', 'd', 'e'];
li // ['a', 'b', 'c', 'd', 'e'] 
li.push('f'); // ['a', 'b', 'c', 'd', 'e', 'f'] : add one element in tail
li.push('f', 'g'); //  ['a', 'b', 'c', 'd', 'e', 'f', 'f', 'g'] : add mult elements in tail
li.concat(['g', 'h']); // ['a', 'b', 'c', 'd', 'e', 'f', 'f', 'g', 'h'] : add mult elements in tail
li.unshift('y', 'z'); // ['y', 'z', 'a', 'b', 'c', 'd', 'e', 'f', 'f', 'g', 'h'] : add one or more elements in head
```

* splice(ind, count, elm1, ... , elmN) : add in middle
ind: staring index
count: 0 === before ind, 1 === delete 1 elem in index and insert elements AND RETURN deleted value
```javascript
var a = ['a', 'b', 'c'];
a.splice(1, 1, 'x', 'y'); // ['a', 'x', 'y', 'c'] --> return b
```

* delete element
```javascript
li = ['a', 'b', 'c'];
li.shift(); // ['b', 'c'] : delete head and return
li.pop(); // ['b'] : delete tail and return
```

* sort elements
```javascript
var li = ['c', 'e', 'a', 'b', 'd'];
li.sort();
alert(li); // a,b,c,d,e

li.reverse();
alert(li); // e,d,c,b,a
```

* Object: index can be any datatype that we define
```javascript
// 3 ways to declare Object
var grades = {'qwe':10, 'asd':40, 'zxc':90}; // define with { }. ' ' called key, things after colon called value
grades // Object {qwe:10, asd:40, zxc:90}

var tier = {};
tier['asd'] = 10;
tier['qwe'] = 20;
tier['zxc'] = 'vbn';

var temp = new Object();
temp['q'] = 'w';
temp['a'] = 1;
```

```javascript

// 2 ways to access value
grades['qwe'] // 10 : key string adjustable: grades['qw'+'e'] 
grades.qwe // 10 : simple

```

* Object with loop
```javascript
var grades = {'asd': 1, 'qwe': 2, 'zxc': 3};
for(key in grades) {
    document.write("key : "+key+" value : "+grades[key]+"<br />");
} // 1,2,3

// for-in can be used in array too
var arr = ['a', 'b', 'c'];
for (var name in arr){
	console.log(name);
	console.log(arr[name]);
} 
```

* Object-Oriented Programming (OOP)
```javascript
// object saved as variable grades have keys 'list' and 'show' with values of object and function

var grades = { 
    'list': {'qwe': 1, 'asd': 3, 'zxc': 5},
    'show' : function(){
        for(var name in this.list){
            document.write(name+':'+this.list[name]+"<br />");
        }
    }
};
// variable "this" indicate object that owns this function
alert(grades['list']['asd']); // 1
alert(grades['show']()); // run function inside of it
grades.show();

```