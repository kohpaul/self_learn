# Web browser and Javascript

* HTML: Epxresses info

```html
<!DOCTYPE html>
<html>
<body>
    <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
    </ul>
</body>
</html>
```

* CSS: Design info

```html
<!DOCTYPE html>
<html>
<head>
    <style type="text/css">
        #selected{
            color:red;
        }
    </style>
</head>
<body>
    <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li id="selected">JavaScript</li>
    </ul>
</body>
</html>
```

* Javascript: Control HTML programmatically

```html
<!DOCTYPE html>
<html>
<head>
    <style type="text/css">
        #selected{
            color:red;
        }
        .dark {
            background-color:black;
            color:white;
        }
        .dark #selected{
            color:yellow;
        }
    </style>
</head>
<body>
    <ul>
        <li>HTML</li>
        <li>CSS</li>
        <li id="selected">JavaScript</li>
    </ul>
    <input type="button" onclick="document.body.className='dark'" value="dark" />
</body>
</html>

```

* Opening local html in chrome on MAC : cmd + o   <- alphabet

# Loading HTML in JavaScript

* inline : Write inside tag
Pro: Straight forward since it's inline
Con: Info and control are mixed : ciritical for maintenance

```html
<!DOCTYPE html>
<html>
<body>
    <input type="button" onclick="alert('Hello world')" value="Hello world" />
</body>
</html>

<!-- onclick="   "        === HTML -->
<!-- alert('Hello world') === JavaScript -->

``` 
* Better to separate HTML and JS w/ <script></script> tag

```html
<!DOCTYPE html>
<html>
<body>
    <input type="button" id="hw" value="Hello world" />
    <script type="text/javascript">
        var hw = document.getElementById('hw');
        hw.addEventListener('click', function(){
            alert('Hello world');
        })
    </script>
</body>
</html>
```

* Even better if we separate HTML and JS with two separate files
1. Info and control separte: better debugging
2. Lesser memory usage
3. Browser download .js as Cache: Do not download that already been downloaded
	1. Significantly reduce network latency
	2. Lesser server burden
	3. Lesser cost
4. Convinience in maintenance: eliminate duplication


* script.html
```html
<!DOCTYPE html>
<html>
<body>
    <input type="button" id="hw" value="Hello world" />
    <script type="text/javascript" src="script2.js"></script>
</body>
</html>
```

* script.js
```javascript
var hw = document.getElementById('hw');
hw.addEventListener('click', function(){
    alert('Hello world');
})
```

* script tag can be on <head></head> tag
window.onload = function(){} : Load every elem in web_browser first, and call function <br>
It is better and faster to place script inside the body tag.

```html
<!DOCTYPE html>
<html>
<head>
    <script src="script2.js"></script>
</head>
<body>
    <input type="button" id="hw" value="Hello world" />
</body>
</html>
```
```javascript
window.onload = function(){
    var hw = document.getElementById('hw');
    hw.addEventListener('click', function(){
        alert('Hello world');
    })
}

```
