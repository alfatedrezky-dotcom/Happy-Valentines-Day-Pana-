<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ultimate SMA Love 💕</title>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.css"/>

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}

body{
  overflow:hidden;
  background:linear-gradient(135deg,#ff758c,#ff7eb3);
  color:white;
  transition:1s;
}

/* LOADING */
#loading{
  position:fixed;
  width:100%;
  height:100vh;
  background:#ff4d88;
  display:flex;
  justify-content:center;
  align-items:center;
  font-size:28px;
  z-index:9999;
  animation:fadeOut 3s forwards 2s;
}

@keyframes fadeOut{
  to{opacity:0;visibility:hidden;}
}

.swiper{width:100%;height:100vh;}

.swiper-slide{
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
  padding:25px;
}

h1{font-size:30px;margin-bottom:15px;}
p{max-width:700px;line-height:1.7;font-size:17px;margin-bottom:15px;}

img{
  width:220px;
  height:320px;
  object-fit:cover;
  border-radius:20px;
  box-shadow:0 0 20px rgba(255,255,255,0.6);
  margin:10px;
  transition:0.4s;
}
img:hover{transform:scale(1.07);}

.typing{
  border-right:3px solid white;
  white-space:nowrap;
  overflow:hidden;
  width:0;
  animation:typing 4s steps(40,end) forwards;
}
@keyframes typing{from{width:0}to{width:100%}}

.hearts{
  position:fixed;
  width:100%;
  height:100%;
  overflow:hidden;
  top:0;
  left:0;
  pointer-events:none;
}
.hearts span{
  position:absolute;
  bottom:-20px;
  width:15px;
  height:15px;
  background:white;
  transform:rotate(45deg);
  animation:float 8s linear infinite;
}
@keyframes float{
  0%{transform:translateY(0) rotate(45deg); opacity:1;}
  100%{transform:translateY(-1000px) rotate(45deg); opacity:0;}
}

.counter{font-size:22px;margin-top:10px;font-weight:bold;}

button{
  padding:15px 30px;
  font-size:18px;
  border:none;
  border-radius:30px;
  cursor:pointer;
  margin:10px;
  transition:0.3s;
}

.yesBtn{background:white;color:#ff4d88;}
.noBtn{background:#ff4d88;color:white;position:relative;}

</style>
</head>
<body>

<div id="loading">Untuk Kamu ❤️</div>
<div class="hearts"></div>

<div class="swiper">
<div class="swiper-wrapper">

<!-- SLIDE 1 -->
<div class="swiper-slide">
<h1 class="typing">Hai Cantikku 💕</h1>
<p>
Kita masih sama-sama pakai seragam,
masih sama-sama belajar,
dan aku seneng banget bisa jalanin masa SMA ini bareng kamu.
</p>
</div>

<!-- SLIDE 2 FOTO -->
<div class="swiper-slide">
<h1>Our Moments 📸</h1>
<img src="foto1.jpg">
<img src="foto2.jpg">
<img src="foto3.jpg">
<p id="lyrics" style="margin-top:15px;font-style:italic;opacity:0;"></p>
</div>

<!-- SLIDE 3 -->
<div class="swiper-slide">
<h1>For You ❤️</h1>
<p>
You are my favorite person in school,
my favorite notification,
and my favorite part of every day.
</p>
<p>
Aku nggak tau masa depan bakal gimana,
tapi sekarang aku bahagia banget sama kamu 💖
</p>
</div>

<!-- SLIDE 4 COUNTER -->
<div class="swiper-slide">
<h1>Udah Berapa Lama Kita? 🥺</h1>
<div class="counter" id="loveCounter"></div>
<p>Dan aku masih mau terus sama kamu 💕</p>
</div>

<!-- SLIDE 5 -->
<div class="swiper-slide">
<h1>Kamu Mau Terus Sama Aku? 🥺💘</h1>
<button class="yesBtn" onclick="jawabYes()">Iya dong 💕</button>
<button class="noBtn" id="noBtn">Hmm... 😳</button>
<p id="jawaban" style="margin-top:20px;font-size:20px;"></p>
</div>

</div>
</div>

<!-- MUSIC -->
<audio id="bgMusic" loop>
<source src="hari-bersamanya.mp3" type="audio/mpeg">
</audio>

<script src="https://cdn.jsdelivr.net/npm/swiper@9/swiper-bundle.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

<script>

var swiper = new Swiper(".swiper",{direction:"horizontal",loop:false});

// HITUNG DARI 5 APRIL 2025
var startDate = new Date("2025-04-05");
var today = new Date();
var diff = today - startDate;
var days = Math.floor(diff / (1000*60*60*24));
document.getElementById("loveCounter").innerHTML =
days + " Hari Bersama ❤️";

// HEART
function createHearts(){
  const container=document.querySelector('.hearts');
  for(let i=0;i<30;i++){
    let heart=document.createElement('span');
    heart.style.left=Math.random()*100+'vw';
    heart.style.animationDuration=5+Math.random()*5+'s';
    heart.style.opacity=Math.random();
    container.appendChild(heart);
  }
}
createHearts();

// MUSIC + LIRIK PAS SLIDE FOTO
var music=document.getElementById("bgMusic");
var lyrics=document.getElementById("lyrics");

swiper.on('slideChange',function(){
  if(swiper.activeIndex===1){
    music.play();
    document.body.style.background=
    "linear-gradient(135deg,#ff4d88,#ff99c8)";
    showLyrics();
  }
});

function showLyrics(){
  lyrics.style.opacity=1;
  var text="Ku menemukanmu saat ku terjatuh...";
  var i=0;
  var typing=setInterval(function(){
    if(i<text.length){
      lyrics.innerHTML+=text.charAt(i);
      i++;
    }else{
      clearInterval(typing);
    }
  },80);
}

// YES BUTTON
function jawabYes(){
  document.getElementById("jawaban").innerHTML=
  "Yeyyy 💖 Aku seneng banget kamu pilih aku 😆💕";
  confetti({particleCount:150,spread:90,origin:{y:0.6}});
}

// NO BUTTON KABUR
var noBtn=document.getElementById("noBtn");
noBtn.addEventListener("mouseover",function(){
  var x=Math.random()*200-100;
  var y=Math.random()*200-100;
  noBtn.style.transform="translate("+x+"px,"+y+"px)";
});

</script>

</body>
</html>
