# HTML
## Web browser and Javascript
### HTML
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

* CSS: Decorate info

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
