<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>hii bb 🦕</title>

<link href="https://fonts.googleapis.com/css2?family=Kite+One&family=Montserrat:wght@500;700&display=swap" rel="stylesheet">

<style>
body {
  background: linear-gradient(#fff1f6, #ffffff);
  text-align: center;
  padding: 50px 20px;
  font-family: 'Montserrat', sans-serif;
  color: #2f2f2f;
  overflow: hidden;
}

h1 {
  font-family: 'Kite One', sans-serif;
  font-size: 46px;
  margin-bottom: 12px;
}

p {
  font-size: 22px;
  line-height: 1.5;
}

button {
  padding: 14px 38px;
  font-size: 18px;
  border-radius: 50px;
  border: none;
  background: #ff7fa8;
  color: white;
  cursor: pointer;
  margin: 14px;
  font-family: 'Montserrat', sans-serif;
  font-weight: 700;
  transition: 0.3s ease;
}

button:hover {
  transform: scale(1.08);
}

#kitty {
  font-size: 54px;
  position: absolute;
  display: none;
  cursor: pointer;
  transition: 1s ease;
}

#thumb {
  width: 130px;
  height: 130px;
  border-radius: 50%;
  border: 3px dashed #ff7fa8;
  display: none;
  margin: 30px auto;
  line-height: 130px;
  font-size: 18px;
  font-weight: 600;
}

#umhmBtn, #ewwBtn {
  display: none;
}

#agreement {
  display: none;
  border: 2px solid #ff7fa8;
  padding: 28px;
  border-radius: 18px;
  font-size: 20px;
  margin-top: 25px;
  font-family: 'Kite One', sans-serif;
}
</style>
</head>

<body>

<h1 id="title">let me tell you something,</h1>
<p id="text">let me tell you something! ✨</p>

<button id="mainBtn">umhm</button>

<div id="kitty">🐱</div>
<div id="thumb">thumb here ✨</div>

<button id="umhmBtn">umhm</button>
<button id="ewwBtn">eww</button>

<div id="agreement">
  <strong>VALENTINE AGREEMENT ✨</strong><br><br>
  i agree to be yours 🤭<br>
  signed already 🧎🏻
</div>

<script>
let catches = 0;
let ewwCount = 0;

const text = document.getElementById("text");
const mainBtn = document.getElementById("mainBtn");
const kitty = document.getElementById("kitty");
const thumb = document.getElementById("thumb");
const umhmBtn = document.getElementById("umhmBtn");
const ewwBtn = document.getElementById("ewwBtn");
const agreement = document.getElementById("agreement");

// STEP 1
mainBtn.onclick = () => {
  mainBtn.style.display = "none";
  text.innerHTML = "ohh wait ✨<br>can you catch this billu for mee once 👉🏽👈🏽";
  kitty.style.display = "block";
  moveKitty();
};

// STEP 2 – BILLU
kitty.onclick = () => {
  catches++;
  moveKitty();
  if (catches === 3) {
    kitty.style.display = "none";
    text.innerHTML = "okay wow 🤭<br>billu trusts you now";
    mainBtn.style.display = "inline-block";
    mainBtn.innerText = "umhmm";
    mainBtn.onclick = () => {
      mainBtn.style.display = "none";
      text.innerHTML = "one tiny thing 🧎🏻<br>place your thumb here real quick";
      thumb.style.display = "block";
    };
  }
};

// STEP 3 – AGREEMENT
thumb.onclick = () => {
  thumb.style.display = "none";
  agreement.style.display = "block";

  setTimeout(() => {
    text.innerHTML = "but wait… 🤭<br>do you even want to 🦕";
    umhmBtn.style.display = "inline-block";
    ewwBtn.style.display = "inline-block";
  }, 1500);
};

// EW RUNS AWAY
ewwBtn.onclick = () => {
  ewwCount++;
  ewwBtn.style.position = "absolute";
  ewwBtn.style.left = Math.random() * 75 + "%";
  ewwBtn.style.top = Math.random() * 75 + "%";

  if (ewwCount === 4) {
    ewwBtn.style.display = "none";
    text.innerHTML = "awww bb 🤭<br>you were already signed anyway 🦕";
  }
};

// FINAL YES
umhmBtn.onclick = () => {
  text.innerHTML = `
    okay then 😗✨<br><br>
    <a href="https://music.youtube.com/watch?v=KdRPDNDNho0&si=H548IT6rO8KrizPs" target="_blank">
      play this ✨
    </a><br><br>
    muahhh 😗✨
  `;
  umhmBtn.style.display = "none";
  ewwBtn.style.display = "none";
};

function moveKitty() {
  kitty.style.left = Math.random() * 70 + "%";
  kitty.style.top = Math.random() * 60 + "%";
}
</script>

</body>
</html>
