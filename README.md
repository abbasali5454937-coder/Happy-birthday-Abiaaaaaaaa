<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday Abia!</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Pacifico&display=swap');

    body {
      margin: 0;
      padding: 0;
      font-family: 'Pacifico', cursive;
      background: linear-gradient(to bottom, #ffe6f2, #ffb3d9);
      overflow-x: hidden;
      text-align: center;
    }

    h1 {
      font-size: 2.5rem;
      color: #ff3399;
      margin-top: 50px;
      animation: bounce 2s infinite;
    }

    p {
      font-size: 1.2rem;
      margin: 20px;
      color: #660033;
    }

    img {
      width: 80%;
      max-width: 300px;
      margin: 20px auto;
      display: block;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
      animation: float 4s ease-in-out infinite;
    }

    @keyframes bounce {
      0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
      40% { transform: translateY(-20px); }
      60% { transform: translateY(-10px); }
    }

    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-15px); }
      100% { transform: translateY(0); }
    }

    /* Confetti */
    .confetti {
      position: fixed;
      top: 0;
      width: 10px;
      height: 10px;
      background-color: #ff3399;
      opacity: 0.7;
      animation: fall 3s linear infinite;
      z-index: 999;
    }

    @keyframes fall {
      0% { transform: translateY(-10px) rotate(0deg); }
      100% { transform: translateY(100vh) rotate(360deg); }
    }
  </style>
</head>
<body>

  <h1>Happy 13th Birthday Abia! 🎉</h1>

  <p>Abia, may your day be filled with laughter, joy, and endless fun! You’re amazing and deserve the best birthday ever. 💖</p>

  <!-- Add your pictures here -->
  <img src="birthday1.jpg" alt="Birthday Pic 1">
  <img src="birthday2.jpg" alt="Birthday Pic 2">

  <!-- Confetti JS -->
  <script>
    const colors = ['#ff3399','#ff66cc','#ff99cc','#ffccff','#ff0066'];
    for(let i=0;i<100;i++){
      let confetti = document.createElement('div');
      confetti.classList.add('confetti');
      confetti.style.left = Math.random() * window.innerWidth + 'px';
      confetti.style.backgroundColor = colors[Math.floor(Math.random()*colors.length)];
      confetti.style.width = confetti.style.height = Math.random() * 10 + 5 + 'px';
      confetti.style.animationDuration = Math.random() * 3 + 2 + 's';
      document.body.appendChild(confetti);
    }
  </script>
</body>
</html>
