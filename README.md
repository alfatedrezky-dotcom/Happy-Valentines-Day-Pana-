# Happy-Valentines-Day-Pana-
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Valentine Sayang ❤️</title>

<style>
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    text-align: center;
    background: linear-gradient(135deg, #ff4e8b, #ff99cc);
    color: white;
    overflow-x: hidden;
}

.container {
    margin-top: 60px;
    padding: 20px;
}

h1 {
    font-size: 40px;
}

.typing {
    font-size: 22px;
    border-right: 3px solid white;
    display: inline-block;
    white-space: nowrap;
    overflow: hidden;
}

.gift {
    font-size: 80px;
    cursor: pointer;
    margin-top: 30px;
    transition: 0.3s;
}

.gift:hover {
    transform: scale(1.2);
}

.hidden {
    display: none;
}

.gallery img {
    width: 180px;
    height: 230px;
    object-fit: cover;
    border-radius: 20px;
    margin: 10px;
    box-shadow: 0 0 20px white;
    transition: 0.3s;
}

.gallery img:hover {
    transform: scale(1.1);
}

button {
    padding: 12px 25px;
    margin: 10px;
    border: none;
    border-radius: 25px;
    font-size: 16px;
    cursor: pointer;
}

.yesBtn {
    background: white;
    color: #ff4e8b;
}

.noBtn {
    background: #ff1a75;
    color: white;
    position: relative;
}

.heart {
    position: fixed;
    top: -10px;
    color: red;
    animation: fall linear forwards;
}

@keyframes fall {
    to { transform: translateY(100vh); }
}

.confetti {
    position: fixed;
    width: 10px;
    height: 10px;
    background: yellow;
    animation: fall linear forwards;
}
</style>
</head>

<body>

<audio id="music" loop>
    <source src="valentine.mp3" type="audio/mpeg">
</audio>

<div class="container">

<h1>Happy Valentine Sayang ❤️</h1>

<div class="typing" id="typing"></div>

<div class="gift" onclick="openGift()">🎁</div>

<div id="surprise" class="hidden">

<!-- SURAT CINTA -->
<div style="max-width:700px; margin:auto; font-size:18px; line-height:1.8; padding:20px;">

<p>Sayangku ❤️,</p>

<p>
Sejak pertama kali aku kenal kamu, hidup aku berubah jadi lebih indah.
You are not just someone I love, you are my comfort, my happiness, and my safe place.
</p>

<p>
Aku mungkin bukan orang yang sempurna,
but every day I try to be better because of you.
</p>

<p>
Kamu adalah alasan aku tersenyum tanpa alasan.
You make my world brighter just by being in it.
</p>

<p>
Aku nggak janji hidup kita akan selalu mudah,
but I promise I will always choose you, again and again.
</p>

<p>
Happy Valentine’s Day, my love 💕
You are my today, my tomorrow, and my forever.
</p>

<p>With all my heart,<br>Your favorite person ❤️</p>

</div>

<!-- GALERI -->
<div class="gallery">
    <img src="foto1.jpg">
    <img src="foto2.jpg">
    <img src="foto3.jpg">
</div>

<!-- REQUEST -->
<h2>Will You Stay With Me Forever? 💍</h2>

<button class="yesBtn" onclick="answerYes()">Yes, Of Course ❤️</button>
<button class="noBtn" id="noBtn" onmouseover="moveButton()">No 😢</button>

<p id="response" style="font-size:20px;"></p>

</div>
</div>

<script>

// Typing Effect
const text = "Untuk Kamu, Cinta Terindah Dalam Hidupku 💖";
let i = 0;
function typingEffect() {
    if (i < text.length) {
        document.getElementById("typing").innerHTML += text.charAt(i);
        i++;
        setTimeout(typingEffect, 80);
    }
}
typingEffect();

// Open Gift + Play Music
function openGift() {
    document.getElementById("surprise").classList.remove("hidden");
    const music = document.getElementById("music");
    music.volume = 0.5;
    music.play();
}

// Falling Hearts
function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 5000);
}
setInterval(createHeart, 300);

// Yes Button
function answerYes(){
    document.getElementById("response").innerHTML =
    "Yayyy ❤️ Aku janji bakal jaga kamu selalu 💕";
    createConfetti();
}

// No Button Kabur
function moveButton(){
    const btn = document.getElementById("noBtn");
    btn.style.position = "absolute";
    btn.style.left = Math.random() * 80 + "vw";
    btn.style.top = Math.random() * 80 + "vh";
}

// Confetti
function createConfetti(){
    for(let i=0;i<50;i++){
        const conf = document.createElement("div");
        conf.classList.add("confetti");
        conf.style.left = Math.random() * 100 + "vw";
        conf.style.background = "hsl(" + Math.random()*360 + ",100%,50%)";
        conf.style.animationDuration = (Math.random()*3+2)+"s";
        document.body.appendChild(conf);
        setTimeout(()=>conf.remove(),5000);
    }
}

</script>

</body>
</html>
