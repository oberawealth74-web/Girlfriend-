<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Be My Valentine ❤️</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      overflow: hidden;
      text-align: center;
    }
    .card {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      max-width: 420px;
      width: 90%;
      position: relative;
      z-index: 2;
    }
    h1 {
      color: #e63946;
    }
    p {
      font-size: 1.1em;
    }
    button {
      padding: 12px 20px;
      margin: 10px;
      border: none;
      border-radius: 30px;
      font-size: 1em;
      cursor: pointer;
      transition: transform 0.2s;
      position: relative;
    }
    button:hover {
      transform: scale(1.05);
    }
    .yes {
      background-color: #e63946;
      color: white;
    }
    .no {
      background-color: #ccc;
    }
    .heart {
      position: absolute;
      color: #e63946;
      font-size: 20px;
      animation: float 6s linear infinite;
      opacity: 0.7;
    }
    @keyframes float {
      from {
        transform: translateY(100vh) scale(1);
      }
      to {
        transform: translateY(-10vh) scale(1.5);
      }
    }
  </style>
</head>
<body>  <audio id="music" autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_58c2b7a4f6.mp3?filename=romantic-love-story-112194.mp3" type="audio/mpeg">
  </audio>  <div class="card" id="content">
    <h1>Hey My Love ❤️</h1>
    <p><strong>Leila</strong>, will you be my Valentine?</p>
    <button class="yes" onclick="sayYes()">Yes 💖</button>
    <button class="no" id="noBtn" onclick="moveNo()">No 🙈</button>
  </div>  <script>
    function sayYes() {
      document.getElementById('content').innerHTML = `
        <h1>Thank You, My Valentine 💕</h1>
        <p>
          Thank you for saying yes, my love ❤️<br><br>
          You mean more to me than words can explain.
          Your smile, your heart, and your presence make my world brighter every single day.
          I’m so grateful to have you, and I can’t wait to celebrate love with you — today and always.
          <br><br>Love always,<br><strong>Wealth</strong> ❤️
        </p>
      `;
    }

    function moveNo() {
      const btn = document.getElementById('noBtn');
      const x = Math.random() * 200 - 100;
      const y = Math.random() * 200 - 100;
      btn.style.transform = `translate(${x}px, ${y}px)`;
    }

    function createHearts() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.innerHTML = '❤️';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.fontSize = Math.random() * 20 + 15 + 'px';
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 6000);
    }

    setInterval(createHearts, 300);
  </script></body>
</html>
