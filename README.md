index.html
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Birthday ❤️</title>

<link rel="stylesheet" href="style.css">

<link href="https://fonts.googleapis.com/css2?family=Itim&family=Great+Vibes&display=swap" rel="stylesheet">

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.2/dist/confetti.browser.min.js"></script>

</head>

<body>

<div id="loading">

    <div class="heart-loader"></div>

    <h2>กำลังเตรียมเซอร์ไพรส์สำหรับเด็กอ้วน...</h2>

</div>


<div id="hearts"></div>

<div id="petals"></div>



<section id="envelopePage">

    <div class="envelope">

        <div class="letter">

            <h1>

                ถึง

            </h1>

            <h2>

                Happy Birthday เด็กอ้วน ❤️

            </h2>

        </div>

        <div class="cover"></div>

    </div>

    <button id="openBtn">

        💌 เปิดจดหมาย

    </button>

</section>



<section id="letterPage">

<div class="glass">

<h1>Happy Birthday 🎂</h1>

<img src="assets/photo.jpg" class="photo">

<div id="typing"></div>

<button id="loveBtn">

💖 กดตรงนี้สิอ้วน

</button>

</div>

</section>



<div id="popup">

<div class="popup-card">

<h1>

❤️

</h1>

<h2>

ขอบคุณที่เข้ามาเป็นความสุขของเค้านะ

</h2>

<p>

ของขวัญที่ดีที่สุดของเค้า...

คือการมีอ้วนอยู่ในทุกๆวัน

</p>

<button id="closePopup">

รักเหมือนกัน 💕

</button>

</div>

</div>



<audio id="openSound">

<source src="https://assets.mixkit.co/active_storage/sfx/2571/2571-preview.mp3">

</audio>



<script src="script.js"></script>

</body>

</html>

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{

font-family:'Itim',cursive;

overflow:hidden;

height:100vh;

background:linear-gradient(135deg,#ffd6e8,#ffeef6,#fff5fb);

display:flex;

justify-content:center;

align-items:center;

}

/* Loading */

#loading{

position:fixed;

width:100%;

height:100%;

background:#ffd8ea;

display:flex;

flex-direction:column;

justify-content:center;

align-items:center;

z-index:9999;

transition:1s;

}

.heart-loader{

width:70px;

height:70px;

background:#ff4f8b;

transform:rotate(-45deg);

animation:beat 1s infinite;

}

.heart-loader:before,
.heart-loader:after{

content:"";

position:absolute;

width:70px;

height:70px;

background:#ff4f8b;

border-radius:50%;

}

.heart-loader:before{

top:-35px;

}

.heart-loader:after{

left:35px;

}

@keyframes beat{

0%{

transform:rotate(-45deg) scale(1);

}

50%{

transform:rotate(-45deg) scale(1.15);

}

100%{

transform:rotate(-45deg) scale(1);

}

}

/* หน้าแรก */

#envelopePage{

display:flex;

flex-direction:column;

align-items:center;

gap:30px;

}

.envelope{

position:relative;

width:340px;

height:230px;

background:#ff8fb4;

border-radius:12px;

box-shadow:0 25px 60px rgba(0,0,0,.25);

overflow:hidden;

}

.cover{

position:absolute;

width:100%;

height:100%;

background:linear-gradient(#ff9ec1,#ff6ea0);

clip-path:polygon(0 0,50% 55%,100% 0,100% 100%,0 100%);

transition:1s;

z-index:3;

}

.letter{

position:absolute;

width:90%;

height:85%;

left:5%;

top:10%;

background:white;

border-radius:12px;

display:flex;

flex-direction:column;

justify-content:center;

align-items:center;

padding:20px;

transition:1s;

z-index:1;

}

.letter h1{

font-family:'Great Vibes';

font-size:55px;

color:#ff3d7b;

}

.letter h2{

font-size:28px;

text-align:center;

color:#ff5b8d;

margin-top:10px;

}

#openBtn{

padding:16px 40px;

font-size:22px;

border:none;

border-radius:50px;

background:#ff5d9e;

color:white;

cursor:pointer;

box-shadow:0 10px 30px rgba(255,0,100,.35);

transition:.3s;

}

#openBtn:hover{

transform:scale(1.08);

}

/* หน้าข้อความ */

#letterPage{

display:none;

position:absolute;

width:100%;

height:100%;

justify-content:center;

align-items:center;

padding:20px;

}

.glass{

width:95%;

max-width:700px;

background:rgba(255,255,255,.35);

backdrop-filter:blur(18px);

border-radius:30px;

padding:30px;

text-align:center;

box-shadow:0 10px 40px rgba(0,0,0,.15);

}

.glass h1{

font-size:45px;

color:#ff3c7b;

margin-bottom:20px;

}

.photo{

width:260px;

border-radius:25px;

box-shadow:0 15px 40px rgba(0,0,0,.25);

margin-bottom:25px;

transition:.4s;

}

.photo:hover{

transform:scale(1.04);

}

#typing{

font-size:22px;

line-height:2;

white-space:pre-line;

color:#444;

margin-bottom:30px;

min-height:250px;

}

#loveBtn{

padding:18px 35px;

font-size:20px;

background:#ff3d82;

color:white;

border:none;

border-radius:50px;

cursor:pointer;

box-shadow:0 10px 25px rgba(255,0,120,.35);

}

/* Popup */

#popup{

display:none;

position:fixed;

width:100%;

height:100%;

background:rgba(0,0,0,.45);

justify-content:center;

align-items:center;

z-index:999;

}

.popup-card{

background:white;

padding:40px;

border-radius:25px;

text-align:center;

max-width:420px;

animation:pop .4s;

}

@keyframes pop{

from{

transform:scale(.5);

opacity:0;

}

to{

transform:scale(1);

opacity:1;

}

}

#closePopup{

margin-top:20px;

padding:14px 25px;

border:none;

background:#ff4c93;

color:white;

border-radius:30px;

cursor:pointer;

}

/* หัวใจลอย */

#hearts{

position:fixed;

width:100%;

height:100%;

pointer-events:none;

overflow:hidden;

}

.heart{

position:absolute;

color:#ff5b93;

font-size:20px;

animation:float 8s linear infinite;

}

@keyframes float{

0%{

transform:translateY(100vh);

opacity:0;

}

10%{

opacity:1;

}

100%{

transform:translateY(-120px);

opacity:0;

}

}

/* Responsive */

@media(max-width:768px){

.glass{

padding:20px;

}

.photo{

width:220px;

}

.letter h1{

font-size:45px;

}

.letter h2{

font-size:22px;

}

#typing{

font-size:18px;

}

}

// =========================
// Loading Screen
// =========================

window.onload = () => {

    setTimeout(() => {

        document.getElementById("loading").style.opacity = "0";

        setTimeout(() => {

            document.getElementById("loading").style.display = "none";

        },1000);

    },2500);

}


// =========================
// Elements
// =========================

const openBtn = document.getElementById("openBtn");

const envelope = document.querySelector(".cover");

const letter = document.querySelector(".letter");

const envelopePage = document.getElementById("envelopePage");

const letterPage = document.getElementById("letterPage");

const typing = document.getElementById("typing");

const popup = document.getElementById("popup");

const loveBtn = document.getElementById("loveBtn");

const closePopup = document.getElementById("closePopup");

const openSound = document.getElementById("openSound");


// =========================
// ข้อความ
// =========================

const message = `

สุขสันต์วันเกิดนะครับอ้วน 🎂

ขอให้อ้วนมีความสุขมากๆ

คิดสิ่งใดขอให้ได้สิ่งนั้น

เป็นคนที่โตขึ้น

มีความสุขมากขึ้น

และการงานที่ดีขึ้น

เป็นเด็กดีน่ารักของพ่อแม่ตลอดไปนะ

ของเค้าด้วย 🤍

เค้ารักอ้วนมากนะครับ

แล้วก็จะรักต่อไปแบบนี้เรื่อยๆ

ไม่มีเปลี่ยน

รักนะครับ 💖

`;


// =========================
// เปิดซองจดหมาย
// =========================

openBtn.onclick = ()=>{

    openSound.play();

    envelope.style.transform="rotateX(180deg)";

    letter.style.transform="translateY(-80px)";

    openBtn.style.display="none";

    setTimeout(()=>{

        envelopePage.style.display="none";

        letterPage.style.display="flex";

        typeWriter();

        launchConfetti();

    },1800);

}


// =========================
// Typewriter
// =========================

let i = 0;

function typeWriter(){

    if(i < message.length){

        typing.innerHTML += message.charAt(i);

        i++;

        setTimeout(typeWriter,45);

    }

}

// =========================
// หัวใจลอย
// =========================

function createHeart(){

    const heart = document.createElement("div");

    heart.className = "heart";

    heart.innerHTML = "❤";

    heart.style.left = Math.random()*100+"vw";

    heart.style.fontSize = (15+Math.random()*35)+"px";

    heart.style.animationDuration = (5+Math.random()*5)+"s";

    document.getElementById("hearts").appendChild(heart);

    setTimeout(()=>{

        heart.remove();

    },10000);

}

setInterval(createHeart,300);


// =========================
// กลีบกุหลาบ
// =========================

function createPetal(){

    const petal = document.createElement("div");

    petal.innerHTML = "🌸";

    petal.style.position="fixed";

    petal.style.left=Math.random()*100+"vw";

    petal.style.top="-50px";

    petal.style.fontSize=(20+Math.random()*20)+"px";

    petal.style.opacity=Math.random();

    petal.style.transition="transform 8s linear";

    petal.style.zIndex="1";

    document.body.appendChild(petal);

    setTimeout(()=>{

        petal.style.transform="translateY(120vh) rotate(720deg)";

    },50);

    setTimeout(()=>{

        petal.remove();

    },9000);

}

setInterval(createPetal,700);


// =========================
// ดาววิบวับ
// =========================

function sparkle(){

    const star=document.createElement("div");

    star.innerHTML="✨";

    star.style.position="fixed";

    star.style.left=Math.random()*100+"vw";

    star.style.top=Math.random()*100+"vh";

    star.style.fontSize=(10+Math.random()*20)+"px";

    star.style.opacity=0;

    star.style.transition=".6s";

    document.body.appendChild(star);

    setTimeout(()=>{

        star.style.opacity=1;

    },100);

    setTimeout(()=>{

        star.style.opacity=0;

    },1200);

    setTimeout(()=>{

        star.remove();

    },1800);

}

setInterval(sparkle,600);


// =========================
// พลุหัวใจ
// =========================

function launchConfetti(){

    confetti({

        particleCount:180,

        spread:120,

        origin:{y:0.6}

    });

}

// =========================
// Popup เมื่อกดปุ่ม
// =========================

loveBtn.onclick = () => {

    popup.style.display = "flex";

    launchConfetti();

    for(let i=0;i<5;i++){

        setTimeout(()=>{
            launchConfetti();
        },i*400);

    }

}


// =========================
// ปิด Popup
// =========================

closePopup.onclick = ()=>{

    popup.style.display="none";

}


// =========================
// ซูมรูป
// =========================

const photo=document.querySelector(".photo");

photo.onclick=()=>{

    if(photo.classList.contains("zoom")){

        photo.classList.remove("zoom");

    }else{

        photo.classList.add("zoom");

    }

}


// =========================
// เพิ่ม CSS สำหรับซูม
// =========================

const style=document.createElement("style");

style.innerHTML=`

.zoom{

position:fixed!important;

top:50%;

left:50%;

transform:translate(-50%,-50%) scale(1.8);

max-width:90vw;

max-height:90vh;

z-index:99999;

cursor:zoom-out;

border-radius:20px;

box-shadow:0 20px 60px rgba(0,0,0,.45);

transition:.4s;

}

`;

document.head.appendChild(style);


// =========================
// Easter Egg
// =========================

let tapCount=0;

document.body.addEventListener("click",()=>{

    tapCount++;

    if(tapCount===5){

        tapCount=0;

        launchConfetti();

        alert("💖 เค้ารักอ้วนที่สุดในโลกเลยนะ 💖");

    }

});


// =========================
// ปุ่มเปิดเพลง
// =========================

const musicBtn=document.createElement("button");

musicBtn.innerHTML="🎵 เปิดเพลง Perfect";

musicBtn.style.position="fixed";

musicBtn.style.bottom="20px";

musicBtn.style.right="20px";

musicBtn.style.padding="15px 25px";

musicBtn.style.borderRadius="50px";

musicBtn.style.border="none";

musicBtn.style.background="#ff4b91";

musicBtn.style.color="white";

musicBtn.style.cursor="pointer";

musicBtn.style.fontSize="18px";

musicBtn.style.boxShadow="0 10px 25px rgba(255,0,120,.3)";

document.body.appendChild(musicBtn);

musicBtn.onclick=()=>{

    window.open(
      "https://www.youtube.com/results?search_query=Perfect+Ed+Sheeran",
      "_blank"
    );

}


// =========================
// ข้อความตอนท้าย
// =========================

setTimeout(()=>{

    const ending=document.createElement("div");

    ending.innerHTML=`

<h1 style="font-family:'Great Vibes';font-size:60px;color:#ff3f82;">
I Love You ❤️
</h1>

<h2 style="margin-top:10px;">
Happy Birthday My Love 🎂
</h2>

`;

    ending.style.position="fixed";

    ending.style.inset="0";

    ending.style.background="rgba(255,255,255,.92)";

    ending.style.display="none";

    ending.style.justifyContent="center";

    ending.style.alignItems="center";

    ending.style.flexDirection="column";

    ending.style.zIndex="999999";

    document.body.appendChild(ending);

    setTimeout(()=>{

        ending.style.display="flex";

        launchConfetti();

    },35000);

},1000);