<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Happy Girlfriend Day Ishika</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(#ffc0cb, #ffe6e6);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      flex-direction: column;
      font-family: 'Segoe UI', sans-serif;
    }
    h1 {
      color: #d6336c;
      text-align: center;
      display: none;
      animation: fadeIn 2s ease-in-out forwards;
    }
    button {
      padding: 15px 30px;
      background-color: #ff4d88;
      color: white;
      border: none;
      border-radius: 30px;
      font-size: 20px;
      cursor: pointer;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }
    .hearts {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
      pointer-events: none;
    }
    .heart {
      position: absolute;
      width: 30px;
      height: 30px;
      background: url('https://img.icons8.com/emoji/48/000000/red-heart.png');
      background-size: cover;
      animation: floatUp 4s linear infinite;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(100vh) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(720deg);
        opacity: 0;
      }
    }

    @keyframes fadeIn {
      to { display: block; opacity: 1; }
    }
  </style>
</head>
<body>
  <button onclick="showMessage()">Tap Here Ishika ❤️</button>
  <h1 id="message">Happy Girlfriend Day, Ishika! 💖<br>
    Tum meri zindagi ki sabse pyaari feeling ho. 💌<br>
    Love You Forever ❤️
  </h1>
  <div class="hearts" id="heartsContainer"></div>

  <script>
    function showMessage() {
      document.querySelector('button').style.display = 'none';
      document.getElementById('message').style.display = 'block';

      for (let i = 0; i < 30; i++) {
        const heart = document.createElement('div');
        heart.classList.add('heart');
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = 2 + Math.random() * 3 + 's';
        document.getElementById('heartsContainer').appendChild(heart);

        setTimeout(() => heart.remove(), 5000);
      }
    }
  </script>
</body>
</html>
