<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love Test ❤️</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, Helvetica, sans-serif;
}

body{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#ff758c,#ff7eb3);
    overflow:hidden;
}

.container{
    text-align:center;
    background:white;
    padding:40px;
    border-radius:20px;
    box-shadow:0 15px 40px rgba(0,0,0,.2);
}

h1{
    color:#ff2e63;
    margin-bottom:15px;
}

p{
    font-size:20px;
    margin-bottom:40px;
}

#ok{
    position:absolute;
    padding:15px 35px;
    font-size:20px;
    border:none;
    border-radius:50px;
    background:#ff2e63;
    color:white;
    cursor:pointer;
    transition:.1s;
}

</style>
</head>

<body>

<div class="container">
    <h1>❤️ Love Test ❤️</h1>
    <p>If you love me, click the OK button 😘</p>
</div>

<button id="ok">OK</button>

<script>

const btn = document.getElementById("ok");

function moveButton(){

    const maxX = window.innerWidth - btn.offsetWidth;
    const maxY = window.innerHeight - btn.offsetHeight;

    const randomX = Math.random() * maxX;
    const randomY = Math.random() * maxY;

    btn.style.left = randomX + "px";
    btn.style.top = randomY + "px";
}

// Initial Position
moveButton();

// Move whenever mouse gets close
btn.addEventListener("mouseenter", moveButton);

// For touch devices
btn.addEventListener("touchstart", function(e){
    e.preventDefault();
    moveButton();
});

</script>

</body>
</html>
