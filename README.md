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
      font-size: 3rem;
      color: #ff3399;
      margin-top: 40px;
      animation: bounce 2s infinite;
      text-shadow: 2px 2px #fff;
    }

    p {
      font-size: 1.4rem;
      margin: 20px 30px;
      color: #660033;
      line-height: 1.6;
      max-width: 800px;
      margin-left: auto;
      margin-right: auto;
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
      opacity: 0.7;
      z-index: 999;
      border-radius: 50%;
      animation: fall linear infinite;
    }

    @keyframes fall {
      0% { transform: translateY(-10px) rotate(0deg); }
      100% { transform: translateY(100vh) rotate(360deg); }
    }

    /* Balloon */
    .balloon {
      position: fixed;
      width: 50px;
      height: 70px;
      border-radius: 50%;
      bottom: -100px;
      animation: balloonMove linear infinite;
      z-index: 998;
    }

    @keyframes balloonMove {
      0% { bottom: -100px; transform: translateX(0) rotate(0deg);}
      100% { bottom: 120%; transform: translateX(100px) rotate(360deg);}
    }

  </style>
</head>
<body>

  <h1>🎉 Happy 13th Birthday Abia! 🎉</h1>

  <p>
    Abia, today is your special day! 🎈 May your 13th birthday be filled with laughter, love, and all the happiness in the world. 
    You deserve to be celebrated in the biggest way possible! 💖 Dance, smile, and enjoy every moment, because you are amazing 
    and your future is as bright as your beautiful heart. Here’s to magical memories, sparkling surprises, and endless fun. 
    Happy Birthday, Abia! May this year bring you countless blessings and unforgettable moments. 🌟🎂
  </p>

  <!-- Online Images -->
  <img src="https://images.unsplash.com/photo-1606788075761-97d73d2e9b02?crop=entropy&cs=tinysrgb&fit=max&w=400&h=400" alt="Birthday Cake">
  <img src="https://images.unsplash.com/photo-1590080870063-742e0a6b2051?crop=entropy&cs=tinysrgb&fit=max&w=400&h=400" alt="Birthday Balloons">

  <!-- Confetti and Balloons JS -->
  <script>
    const colors = ['#ff3399','#ff66cc','#ff99cc','#ffccff','#ff0066','#ff66ff'];

    // Confetti
    for(let i=0;i<100;i++){
      let confetti = document.createElement('div');
      confetti.classList.add('confetti');
      confetti.style.left = Math.random() * window.innerWidth + 'px';
      confetti.style.backgroundColor = colors[Math.floor(Math.random()*colors.length)];
      confetti.style.width = confetti.style.height = Math.random() * 10 + 5 + 'px';
      confetti.style.animationDuration = Math.random() * 3 + 2 + 's';
      document.body.appendChild(confetti);
    }

    // Balloons
    for(let i=0;i<10;i++){
      let balloon = document.createElement('div');
      balloon.classList.add('balloon');
      balloon.style.left = Math.random()*window.innerWidth + 'px';
      balloon.style.animationDuration = 5 + Math.random()*5 + 's';
      balloon.style.background = `radial-gradient(circle at 30% 30%, ${colors[Math.floor(Math.random()*colors.length)]}, #fff)`;
      document.body.appendChild(balloon);
    }
  </script>

</body>
</html>
