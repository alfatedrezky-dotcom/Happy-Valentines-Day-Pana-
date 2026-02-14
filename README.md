<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Will You Be Mine? ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Poppins&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif;}

body{
  background:#7b0000;
  color:white;
  overflow-x:hidden;
}

/* SECTION STYLE */
.section{
  min-height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
  padding:40px 20px;
}

/* HEADER */
.title{
  font-family:'Playfair Display',serif;
  font-size:40px;
}

.subtitle{
  font-size:20px;
  margin-bottom:20px;
}

/* FRAME FOTO */
.gallery{
  display:flex;
  gap:20px;
  flex-wrap:wrap;
  justify-content:center;
}

.frame{
  background:#a10000;
  padding:10px;
  border:8px solid gold;
  border-radius:15px;
}

.frame img{
  width:200px;
  height:250px;
  object-fit:cover;
  border-radius:10px;
}

/* SURAT */
.letter{
  background:#fff5f5;
  color:#333;
  padding:30px;
  border-radius:10px;
  max-width:600px;
  font-size:15px;
  line-height:1.7;
  box-shadow:0 10px 30px rgba(0,0,0,0.4);
}

/* HEART SECTION */
.big-heart{
  font-size:120px;
  color:#ff2e63;
  animation:beat 1s infinite;
}

@keyframes beat{
  0%,100%{transform:scale(1);}
  50%{transform:scale(1.1);}
}

/* SAVE DATE */
.date-box{
  background:#8b0000;
  padding:30px;
  border-radius:20px;
  font-size:20px;
}

/* BUTTON */
button{
  padding:15px 30px;
  font-size:18px;
  border:none;
  border-radius:30px;
  cursor:pointer;
  margin-top:20px;
}

.yes{background:white;color:#7b0000;}
.no{background:#ff2e63;color:white;position:relative;}

</style>
</head>
<body>

<!-- SECTION 1 -->
<div class="section">
  <div class="subtitle">sooo...</div>
  <div class="title">Will You Be My Valentine? ❤️</div>
</div>

<!-- SECTION 2 FOTO -->
<div class="section">
  <h2 style="margin-bottom:20px;">us being cute n stuff 📸</h2>
  <div class="gallery">
    <div class="frame"><img src="foto1.jpg"></div>
    <div class="frame"><img src="foto2.jpg"></div>
    <div class="frame"><img src="foto3.jpg"></div>
  </div>
</div>

<!-- SECTION 3 SURAT -->
<div class="section">
  <div class="letter">
    <h3 style="font-family:'Playfair Display',serif;">hey you 🤍</h3>
    <p>
      i don’t really know how to say this without sounding cringe,
      but you matter to me. like… for real.
    </p>
    <p>
      sekolah jadi lebih seru since i met you.
      ngobrol random, ketawa ga jelas,
      bahkan tugas yang bikin stress pun
      jadi kerasa lighter when i'm with you.
    </p>
    <p>
      i’m not promising some movie-type romance,
      but i promise i’ll stay,
      stay caring,
      stay choosing you.
    </p>
    <p>
      so yeah…
      happy valentine’s day, pretty 💌
    </p>
  </div>
</div>

<!-- SECTION 4 HEART -->
<div class="section">
  <div class="big-heart">❤️</div>
  <h2>would you keep vibing with me?</h2>

  <button class="yes" onclick="yesClick()">obviously yes 😌</button>
  <button class="no" id="noBtn">hmm...</button>

  <p id="answer" style="margin-top:20px;font-size:18px;"></p>
</div>

<!-- SECTION 5 SAVE DATE -->
<div class="section">
  <div class="date-box">
    <h2 style="font-family:'Playfair Display',serif;">our special day</h2>
    <p>5 April 2025</p>
    <p>still counting the days together 💞</p>
  </div>
</div>

<script>

// YES BUTTON
function yesClick(){
  document.getElementById("answer").innerHTML =
  "hehe i knew it 😎💘 we're kinda iconic ngl";
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
