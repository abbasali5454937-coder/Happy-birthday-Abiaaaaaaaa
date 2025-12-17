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
      position: relative;
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
      animation: fadeIn 3s ease-in;
    }

    @keyframes bounce {
      0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
      40% { transform: translateY(-20px); }
      60% { transform: translateY(-10px); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    /* Confetti */
    .confetti {
      position: fixed;
      top: 0;
      width: 10px;
      height: 10px;
      opacity: 0.8;
      z-index: 999;
      border-radius: 50%;
      animation: fall linear infinite;
    }

    @keyframes fall {
      0% { transform: translateY(-10px) rotate(0deg); }
      100% { transform: translateY(100vh) rotate(360deg); }
    }

    /* Balloons */
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

    /* Sparkles */
    .sparkle {
      position: fixed;
      width: 5px;
      height: 5px;
      background: gold;
      border-radius: 50%;
      opacity: 0.8;
      animation: sparkleMove 2s infinite;
      z-index: 1000;
    }

    @keyframes sparkleMove {
      0% { transform: translateY(0) scale(1); opacity: 1; }
      50% { transform: translateY(-20px) scale(1.5); opacity: 0.5; }
      100% { transform: translateY(0) scale(1); opacity: 1; }
    }

  </style>
</head>
<body>

  <h1>🎉 Happy 13th Birthday Abia! 🎉</h1>

  <p>
    Abia, today is all about YOU! 🎈 May your 13th birthday sparkle with joy, laughter, and magical moments. 
    This year, may you discover new adventures, create beautiful memories, and shine brighter than ever before. 💖 
    Dance, laugh, and celebrate with all your heart, because you are truly special and deserve the best. 
    Here’s to endless fun, magical surprises, and the happiest birthday ever! 🌟🎂
  </p>

  <p>
    You are amazing, Abia! May your 13th year bring you endless smiles, exciting adventures, and dreams come true. 
    Always remember, you are loved, cherished, and celebrated every single day. 🎁✨ Let’s make this birthday unforgettable!
  </p>

  <!-- Confetti and Balloons JS -->
  <script>
    const colors = ['#ff3399','#ff66cc','#ff99cc','#ffccff','#ff0066','#ff66ff','#ff99ff','#ffb3e6'];

    // Confetti
    for(let i=0;i<150;i++){
      let confetti = document.createElement('div');
      confetti.classList.add('confetti');
      confetti.style.left = Math.random() * window.innerWidth + 'px';
      confetti.style.backgroundColor = colors[Math.floor(Math.random()*colors.length)];
      confetti.style.width = confetti.style.height = Math.random() * 10 + 5 + 'px';
      confetti.style.animationDuration = Math.random() * 3 + 2 + 's';
      document.body.appendChild(confetti);
    }

    // Balloons
    for(let i=0;i<15;i++){
      let balloon = document.createElement('div');
      balloon.classList.add('balloon');
      balloon.style.left = Math.random()*window.innerWidth + 'px';
      balloon.style.animationDuration = 5 + Math.random()*5 + 's';
      balloon.style.background = `radial-gradient(circle at 30% 30%, ${colors[Math.floor(Math.random()*colors.length)]}, #fff)`;
      document.body.appendChild(balloon);
    }

    // Sparkles
    for(let i=0;i<50;i++){
      let sparkle = document.createElement('div');
      sparkle.classList.add('sparkle');
      sparkle.style.left = Math.random()*window.innerWidth + 'px';
      sparkle.style.top = Math.random()*window.innerHeight + 'px';
      sparkle.style.animationDuration = 1 + Math.random()*2 + 's';
      document.body.appendChild(sparkle);
    }
  </script>

</body>
</html>
