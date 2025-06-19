<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Happy Birthday Bk!</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@600&display=swap');

  html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Poppins', sans-serif;
    overflow: hidden;
    background: white;
  }

  #landing {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: white;
  }

  #birthday-button {
    background: #e63946;
    border: none;
    border-radius: 15px;
    color: white;
    font-size: 2.5rem;
    padding: 1.5rem 3rem;
    cursor: pointer;
    box-shadow: 0 8px 15px rgba(230, 57, 70, 0.4);
    transition: background 0.3s ease;
  }

  #birthday-button:hover {
    background: #d62828;
  }

  #main {
    display: none;
    position: relative;
    height: 100vh;
    background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
    overflow: hidden;
    color: #333;
    text-align: center;
    padding-top: 3rem;
  }

  #message {
    position: relative;
    font-size: 3rem;
    font-weight: 700;
    margin-bottom: 2rem;
    color: #222;
    text-shadow: 0 0 8px #f72585, 0 0 15px #720026;
  }

  /* Stars and hearts around message */
  .decor {
    position: absolute;
    font-size: 1.5rem;
    color: #f72585;
    animation: twinkle 3s infinite ease-in-out;
  }

  @keyframes twinkle {
    0%, 100% {opacity: 1;}
    50% {opacity: 0.3;}
  }

  /* Randomly position stars and hearts */
  #decor1 { top: 60px; left: 40%; animation-delay: 0s; }
  #decor2 { top: 110px; right: 38%; animation-delay: 1s; }
  #decor3 { top: 50px; left: 48%; animation-delay: 2s; }
  #decor4 { top: 120px; right: 45%; animation-delay: 2.5s; }

  /* Dolphin swimming animation */
  .dolphin {
    position: absolute;
    width: 120px;
    height: 60px;
    background: url('https://i.imgur.com/6W7GztZ.png') no-repeat center/contain;
    animation-timing-function: linear;
  }

  /* Multiple dolphins with different paths */
  #dolphin1 {
    top: 60vh;
    left: -150px;
    animation: swimRight 20s linear infinite;
  }
  #dolphin2 {
    top: 40vh;
    left: -200px;
    animation: swimRight 25s linear infinite;
    animation-delay: 5s;
  }
  #dolphin3 {
    top: 75vh;
    left: -170px;
    animation: swimRight 30s linear infinite;
    animation-delay: 10s;
  }

  @keyframes swimRight {
    0% { left: -150px; transform: scaleX(1) translateY(0);}
    50% { transform: scaleX(1) translateY(10px);}
    100% { left: 110vw; transform: scaleX(1) translateY(0);}
  }

  /* Water splashes */
  .splash {
    position: absolute;
    width: 50px;
    height: 50px;
    background: url('https://i.imgur.com/bUzQ7lh.png') no-repeat center/contain;
    opacity: 0.6;
    animation: splashAnim 4s ease-in-out infinite;
  }

  /* Different positions for splashes */
  #splash1 { top: 70vh; left: 30vw; animation-delay: 0s; }
  #splash2 { top: 80vh; left: 50vw; animation-delay: 2s; }
  #splash3 { top: 60vh; left: 70vw; animation-delay: 3s; }

  @keyframes splashAnim {
    0%, 100% {opacity: 0.6;}
    50% {opacity: 0;}
  }

  /* Hearts */
  .heart {
    position: absolute;
    width: 50px;
    height: 50px;
    background: url('https://i.imgur.com/R1HxRPr.png') no-repeat center/contain;
    animation: floatUp 8s linear infinite;
  }

  #heart1 {
    bottom: 5vh;
    left: 20vw;
    animation-delay: 0s;
  }
  #heart2 {
    bottom: 10vh;
    left: 65vw;
    animation-delay: 3s;
  }

  @keyframes floatUp {
    0% {transform: translateY(0);}
    100% {transform: translateY(-100vh);}
  }

  /* YouTube player style - hidden controls */
  #music {
    position: fixed;
    bottom: 10px;
    right: 10px;
    width: 300px;
    height: 170px;
    border-radius: 12px;
    box-shadow: 0 0 15px rgba(0,0,0,0.3);
  }
</style>
</head>
<body>
<div id="landing">
  <button id="birthday-button">happy birthday cutie patootie</button>
</div>

<div id="main">
  <div id="message">
    happy birthday Bk!!
    <span id="decor1" class="decor">⭐</span>
    <span id="decor2" class="decor">❤️</span>
    <span id="decor3" class="decor">⭐</span>
    <span id="decor4" class="decor">❤️</span>
  </div>

  <!-- Dolphins -->
  <div id="dolphin1" class="dolphin"></div>
  <div id="dolphin2" class="dolphin"></div>
  <div id="dolphin3" class="dolphin"></div>

  <!-- Water splashes -->
  <div id="splash1" class="splash"></div>
  <div id="splash2" class="splash"></div>
  <div id="splash3" class="splash"></div>

  <!-- Hearts -->
  <div id="heart1" class="heart"></div>
  <div id="heart2" class="heart"></div>

  <!-- YouTube live music embed -->
  <iframe id="music" src="https://www.youtube.com/embed/9vH5ZBh1-_g?autoplay=1&loop=1&playlist=9vH5ZBh1-_g&controls=0&mute=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>

<script>
  const button = document.getElementById('birthday-button');
  const landing = document.getElementById('landing');
  const main = document.getElementById('main');

  button.addEventListener('click', () => {
    landing.style.display = 'none';
    main.style.display = 'block';
  });
</script>
</body>
</html>
