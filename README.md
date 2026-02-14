<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Our SMA Love Story 💖</title>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css"/>

<style>
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #ff4e88, #ff9ac6);
  overflow: hidden;
  color: white;
  text-align: center;
}

.swiper {
  width: 100%;
  height: 100vh;
}

.swiper-slide {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

img {
  width: 80%;
  max-width: 300px;
  border-radius: 20px;
  box-shadow: 0 0 30px rgba(255,255,255,0.6);
  margin-bottom: 20px;
}

h1 {
  font-size: 28px;
  margin-bottom: 10px;
}

p {
  font-size: 16px;
  max-width: 300px;
}

.counter {
  font-size: 20px;
  margin-top: 15px;
  font-weight: bold;
}

.hearts {
  position: absolute;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: -1;
}

.heart {
  position: absolute;
  color: rgba(255,255,255,0.3);
  font-size: 20px;
  animation: float 10s infinite linear;
}

@keyframes float {
  0% {transform: translateY(100vh);}
  100% {transform: translateY(-10vh);}
}
</style>
</head>

<body>

<div class="hearts"></div>

<div class="swiper">
  <div class="swiper-wrapper">

    <!-- Slide 1 -->
    <div class="swiper-slide">
      <h1>Hi Cantik 💕</h1>
      <p>
        Ga nyangka ya kita masih bareng sampai sekarang…  
        still strong, still crazy, still us 😌💖
      </p>
    </div>

    <!-- Slide 2 -->
    <div class="swiper-slide">
      <img src="IMG-20251101-WA0457.jpg">
      <p>
        Every moment sama kamu tuh vibes nya beda banget.  
        Kayak dunia auto slow motion tiap liat kamu 😆✨
      </p>
    </div>

    <!-- Slide 3 -->
    <div class="swiper-slide">
      <img src="IMG-20250907-WA0503.jpg">
      <p>
        Makasih ya udah stay,  
        walaupun aku kadang ngeselin dikit 🤏😂  
        but you still choose me.
      </p>
    </div>

    <!-- Slide 4 -->
    <div class="swiper-slide">
      <img src="IMG-20250909-WA0444.jpg">
      <p>
        Kita masih SMA, masih banyak mimpi,  
        but I’m really happy I get to grow with you 🫶
      </p>
      <div class="counter" id="counter"></div>
    </div>

    <!-- Slide 5 -->
    <div class="swiper-slide">
      <h1>I Love You 💗</h1>
      <p>
        Ga perlu janji gede-gede.  
        Yang penting kita terus bareng,  
        support each other, and stay loyal 💍✨  
        You’re my favorite person, always.
      </p>

      <br>

      <!-- Spotify Lagu Hari Bersamanya -->
      <iframe style="border-radius:12px" 
      src="https://open.spotify.com/embed/track/2Z8WuEywRWYTKe1NybPQEW?utm_source=generator" 
      width="300" height="80" frameBorder="0" 
      allowfullscreen="" 
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
      </iframe>
    </div>

  </div>
</div>

<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>

<script>
const swiper = new Swiper('.swiper', {
  direction: 'horizontal',
  loop: false,
});

const startDate = new Date("2025-04-05");
const today = new Date();
const diffTime = today - startDate;
const diffDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));

document.getElementById("counter").innerHTML =
  "Udah bareng " + diffDays + " hari dan counting terus 💕🔥";

// Floating hearts
const heartsContainer = document.querySelector('.hearts');
for (let i = 0; i < 30; i++) {
  let heart = document.createElement('div');
  heart.classList.add('heart');
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = Math.random() * 20 + 10 + "px";
  heart.innerHTML = "❤";
  heartsContainer.appendChild(heart);
}
</script>

</body>
</html>
