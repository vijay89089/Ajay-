
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sorry My Bestie 💗</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  min-height: 100vh;
  overflow-x: hidden;
  font-family: "Trebuchet MS", sans-serif;
  background: linear-gradient(135deg, #ffd1dc, #ffe6f0, #e7c6ff);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 25px 12px;
}

.card {
  width: 100%;
  max-width: 400px;
  text-align: center;
  background: rgba(255,255,255,0.8);
  border: 2px solid white;
  border-radius: 30px;
  padding: 28px 22px;
  box-shadow: 0 15px 45px #d65b9c40;
  position: relative;
  z-index: 2;
}

.tag {
  display: inline-block;
  background: #ffe0eb;
  color: #d63384;
  padding: 7px 15px;
  border-radius: 20px;
  font-size: 13px;
}

.teddy {
  font-size: 90px;
  margin: 15px 0;
  animation: bounce 2s infinite;
}

h1 {
  color: #e84393;
  font-size: 32px;
  margin-bottom: 12px;
}

p {
  color: #755267;
  font-size: 16px;
  line-height: 1.8;
}

.letter {
  background: #fff5fa;
  padding: 16px;
  margin: 20px 0;
  border-radius: 18px;
  border: 1px dashed #f29ac2;
}

button {
  border: none;
  border-radius: 30px;
  padding: 13px 19px;
  margin: 6px 3px;
  font-size: 15px;
  font-weight: bold;
  cursor: pointer;
  transition: 0.25s;
}

button:hover {
  transform: scale(1.05);
}

.yes {
  background: linear-gradient(45deg, #ff4f91, #ff78ac);
  color: white;
  box-shadow: 0 5px 15px #ff4f9150;
}

.read {
  background: white;
  color: #d63384;
  border: 1px solid #ffc0d9;
}

#reply {
  color: #d63384;
  font-size: 17px;
  font-weight: bold;
  margin-top: 17px;
  line-height: 1.7;
}

#letterText {
  display: none;
  margin-top: 12px;
}

.footer {
  font-size: 12px;
  margin-top: 20px;
  color: #ad7c9a;
}

.heart {
  position: fixed;
  bottom: -30px;
  pointer-events: none;
  animation: rise linear forwards;
  z-index: 1;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0) rotate(-3deg); }
  50% { transform: translateY(-10px) rotate(3deg); }
}

@keyframes rise {
  to {
    transform: translateY(-110vh) rotate(30deg);
    opacity: 0;
  }
}
</style>
</head>

<body>

<div class="card">
  <span class="tag">💌 A Little Message For You</span>

  <div class="teddy">🧸💗</div>

  <h1>I'm Sorry, Bestie! 🥺</h1>

  <p>
    Heyyy, my favourite human! 🌷<br>
    Please ek baar meri baat sun lo...
  </p>

  <div class="letter">
    <p>
      Mujhse galti ho gayi toh<br>
      <b>I'm really sorry! 🥹❤️</b><br>
      Tumhari friendship mere liye<br>
      bahut special hai. 🫶
    </p>

    <div id="letterText">
      <p>
        💌 Dear Bestie,<br><br>
        Main nahi chahta/chahti ki ek chhoti si
        misunderstanding humari beautiful friendship
        ko hurt kare. Agar meri kisi baat se tumhe
        bura laga, toh dil se sorry. ❤️<br><br>
        Jab tum ready ho, hum baat kar sakte hain.
        No pressure. Tumhari feelings mere liye
        important hain. 🫂💗<br><br>
        <b>Always your friend! 🌸</b>
      </p>
    </div>
  </div>

  <button class="read" onclick="showLetter()">
    💌 Open My Letter
  </button>

  <br>

  <button class="yes" onclick="forgive()">
    Maaf Kiya ❤️
  </button>

  <div id="reply"></div>

  <div class="footer">
    Made with love, just for you 💗
  </div>
</div>

<script>
function showLetter() {
  const letter = document.getElementById("letterText");
  letter.style.display =
    letter.style.display === "block" ? "none" : "block";
}

function makeHearts() {
  const emojis = ["💗", "💕", "💖", "🌸", "🫶", "❤️"];

  for (let i = 0; i < 35; i++) {
    setTimeout(() => {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.textContent =
        emojis[Math.floor(Math.random() * emojis.length)];

      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (16 + Math.random() * 22) + "px";
      heart.style.animationDuration = (3 + Math.random() * 4) + "s";

      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 7500);
    }, i * 60);
  }
}

function forgive() {
  document.getElementById("reply").innerHTML =
    "Yayyy! 🥹💗<br>" +
    "Thank you, Bestie! 🫂💕<br>" +
    "A big virtual hug for you! 🤗🌷";

  makeHearts();
}
</script>

</body>
</html>
