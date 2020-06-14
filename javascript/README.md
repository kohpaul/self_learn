Javascript

<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8"/>
    </head>
    <body>
        <script>
            alert('Hello world');
        </script>
    </body>
</html>

// MAC chrome developer mode : cmd+alt+j

// numbers auto cast
alert(1+1.0);	// 2
alert(Math.pow(3,2));	// 9

alert(typeof “1”);	// string
alert(typeof 1);	// number 
alert(‘shaun\’s javascript’);	// shaun’s javascript
alert("coding"+" everybody");	// coding everybody
alert("coding everybody".length);	// 16

//declaration
var a = 1; var b;

// assign operator
=

// equal operator 
== 
alert(1 == “1”);	// true

// strict equal operator
===
alert(1 === “1”);	// false

// undefined: not intended  none value. undefined is a datatype
// null : intended none value. null is a datatype

alert(null == undefined);       //true
alert(null === undefined);      //false
alert(true == 1);               //true
alert(true === 1);              //false
alert(true == '1');             //true
alert(true === '1');            //false
 
alert(0 === -0);                //true
alert(NaN === NaN);             //false

// not equal
!=

// strictly not equal
!==

// conditional statement
if (false){
	alert(1);
} else if (true) {
	alert(2);
} else if (true) {
	alert(3);
} else {
	alert(4);
}   // 2 —>  3 이전에 조건 만족했으므로 3까지 안감


// get user input
prompt(‘your age?’); 
alert(prompt(‘your age?’)); // 20

// Logic operator 
&&
||

// can use more than 2
if (true && true && false || true){
	statement
}

break; // === out of loop
continue; // === skip and continue loop



 

