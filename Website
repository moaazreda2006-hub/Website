<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Moaaz Reda</title>

<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;600;800&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Cairo',sans-serif;
}

body{
    background:#050505;
    overflow:hidden;
    color:white;
}

/* خلفية متحركة */

canvas{
    position:fixed;
    top:0;
    left:0;
    z-index:-1;
}

/* شاشة البداية */

.loader{
    position:fixed;
    width:100%;
    height:100vh;
    background:black;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    z-index:9999;
    animation:hideLoader 4s forwards;
}

.loader h1{
    color:#00ff88;
    font-size:40px;
    text-shadow:0 0 15px #00ff88;
    animation:glow 1s infinite alternate;
    text-align:center;
    padding:20px;
}

.loader p{
    color:white;
    margin-top:10px;
    font-size:20px;
}

@keyframes glow{
    from{
        text-shadow:0 0 10px #00ff88;
    }
    to{
        text-shadow:0 0 25px #00ff88,
                     0 0 50px #00ff88;
    }
}

@keyframes hideLoader{
    0%,85%{
        opacity:1;
        visibility:visible;
    }

    100%{
        opacity:0;
        visibility:hidden;
    }
}

/* المحتوى */

.container{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    text-align:center;
    width:90%;
}

.logo{
    font-size:70px;
    color:#00ff88;
    font-weight:800;
    text-shadow:0 0 20px #00ff88;
    animation:flicker 2s infinite;
}

@keyframes flicker{
    0%,18%,22%,25%,53%,57%,100%{
        opacity:1;
    }

    20%,24%,55%{
        opacity:0.4;
    }
}

.bio{
    margin-top:15px;
    color:#ccc;
    font-size:22px;
}

/* الأزرار */

.buttons{
    margin-top:40px;
}

.btn{
    display:inline-block;
    margin:10px;
    padding:14px 30px;
    border:2px solid #00ff88;
    color:#00ff88;
    text-decoration:none;
    border-radius:12px;
    transition:0.3s;
    font-size:18px;
    backdrop-filter:blur(10px);
}

.btn:hover{
    background:#00ff88;
    color:black;
    box-shadow:0 0 20px #00ff88;
    transform:scale(1.05);
}

/* الفوتر */

.footer{
    position:absolute;
    bottom:20px;
    width:100%;
    text-align:center;
    color:#777;
    font-size:15px;
}

/* Responsive */

@media(max-width:700px){

.logo{
    font-size:45px;
}

.bio{
    font-size:18px;
}

.loader h1{
    font-size:28px;
}

}

</style>
</head>

<body>

<!-- شاشة البداية -->

<div class="loader">
    <h1>تم تصميم الموقع بواسطة المهندس معاذ رضا</h1>
    <p>Loading Secure System...</p>
</div>

<!-- خلفية Matrix -->

<canvas id="matrix"></canvas>

<!-- المحتوى -->

<div class="container">

    <div class="logo">
        MOAAZ REDA
    </div>

    <div class="bio">
        Cyber Security | Red Team | Developer
    </div>

    <div class="buttons">

        <a href="#" class="btn">Facebook</a>

        <a href="#" class="btn">GitHub</a>

        <a href="#" class="btn">Telegram</a>

        <a href="#" class="btn">TikTok</a>

    </div>

</div>

<div class="footer">
    © 2026 | Designed By Engineer Moaaz Reda
</div>

<script>

/* Matrix Effect */

const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const letters = "01";
const fontSize = 14;
const columns = canvas.width / fontSize;

const drops = [];

for(let x = 0; x < columns; x++){
    drops[x] = 1;
}

function draw(){

    ctx.fillStyle = "rgba(0,0,0,0.05)";
    ctx.fillRect(0,0,canvas.width,canvas.height);

    ctx.fillStyle = "#00ff88";
    ctx.font = fontSize + "px monospace";

    for(let i = 0; i < drops.length; i++){

        const text = letters[Math.floor(Math.random()*letters.length)];

        ctx.fillText(text,i*fontSize,drops[i]*fontSize);

        if(drops[i]*fontSize > canvas.height && Math.random() > 0.975){
            drops[i] = 0;
        }

        drops[i]++;
    }
}

setInterval(draw,35);

window.addEventListener("resize",()=>{
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
});

</script>

</body>
</html>
