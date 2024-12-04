# ⏰Часы с подсветкой на JavaScript⏲

![2024-12-04_11-24-20](https://github.com/user-attachments/assets/7b0f31bd-8edc-4d7c-bb2a-11ef568e33e8)


1. Шрифты скачать с google fonts - https://fonts.google.com/
2. В файле Clock_CSS.css

```CSS
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');  
  
body{  
    background: #242327;  
}  
#clock{  
    position: absolute;  
    top: 50%;  
    left: 40%;  
    margin: -125px 0 0 -125px;  
    font-family: "Share Tech Mono", monospace;  
    font-size: 200px;  
    color: #dfdede;  
    text-shadow: 0 0 50px #003eff;  
    border: double #fbfbfb;  
    box-shadow: 0 0 50px #003eff;  
}
```

![2024-12-04_11-29-24](https://github.com/user-attachments/assets/2c7c0b01-fd10-4a92-8197-d3c794017483)


3. В файле Clock_HTML.html

```HTML
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Часики</title>  
    <link rel="stylesheet" href="Clock_CSS.css">  
</head>  
<body>  
<script src="Clock_JS.js"></script>  
<div id="clock"></div>  
</body>  
</html>
```

![2024-12-04_11-30-46](https://github.com/user-attachments/assets/ae3eb030-f7bc-485b-b0e9-f93e35f19814)


4. В файле Clock_JS.js

```JavaScript
setInterval(function(){  
    var date = new Date();  
  
    var format = [  
        (date.getHours()<10 ? "0"+date.getHours() : date.getHours()),  
        (date.getMinutes()<10 ? "0"+date.getMinutes() : date.getMinutes()),  
        (date.getSeconds()<10 ? "0"+date.getSeconds() : date.getSeconds())  
    ].join(":")  
  
    document.getElementById("clock").innerHTML = format;  
}, 10);
```

![2024-12-04_11-31-56](https://github.com/user-attachments/assets/b5108dec-b8cb-4a85-b655-48ebc5b307da)

