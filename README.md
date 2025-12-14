<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio</title>

  <!-- Bootstrap 5 CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"/>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet"/>

  <style>
    body { font-family: "Poppins", sans-serif; }

    /* Keep page anchors from hiding behind the fixed navbar */
    html { scroll-padding-top: 80px; }

    /* Ensure the hero keeps space for the fixed navbar */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      background: radial-gradient(circle at top left, #ffeaf1, transparent), 
                  radial-gradient(circle at bottom right, #fff6d7, transparent);
      padding-top: 80px;
    }

    .btn-pill {
      border-radius: 50px;
      padding: 0.6rem 1.4rem;
    }

    .navbar.fixed-top { box-shadow: 0 2px 8px rgba(0,0,0,0.06); }
  </style>
</head>

<body>

<nav class="navbar navbar-expand-lg bg-white shadow-sm py-3 fixed-top">
  <div class="container">
    <a class="navbar-brand fw-bold" href="#">
      Portfolio
    </a>

    <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#nav">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="nav">
      <ul class="navbar-nav mx-auto">
        <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
        <li class="nav-item"><a class="nav-link" href="#resume">Resume</a></li>
        <li class="nav-item"><a class="nav-link" href="#portfolio">Portfolio</a></li>
        <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
      </ul>
    </div>
  </div>
</nav>

<header class="hero" id="home">
  <div class="container">
    <div class="row align-items-center">

      <div class="col-lg-6">
        <p class="text-muted mb-1">Hi,</p>

        <h1 class="fw-bold">I'm <span> Allexy Casandra Teoco</span></h1>

        <h2 class="fw-bold text-danger">
          Web Designer & Developer
        </h2>

        </p>

        <div class="d-flex gap-3 mt-4">
          <a href="#contact" class="btn btn-primary btn-pill">Hire Me</a>
        </div>
      </div>

      <div class="col-lg-6 mt-5 mt-lg-0">
        <img 
          src="profile.png" 
          class="img-fluid rounded-4"
          alt="Your Photo Here"
        />
      </div>

    </div>
  </div>
</header>

<!-- ABOUT SECTION -->
<section id="about" class="py-5">
  <div class="container">
    <h2 class="fw-bold mb-4">About Me</h2>

    <p>
      <!-- Write your full 'About Me' paragraph here -->
      I have basic knowledge in web design, coding and technology. I am eager to know more about how digital systems work.
    </p>

  </div>
</section>

<!-- RESUME SECTION -->
<section id="resume" class="py-5 bg-light">
  <div class="container">
    <h2 class="fw-bold text-center mb-5">Resume</h2>

    <div class="row">
      <div class="col-md-6">
        <h4>Experience</h4>

        <div class="mt-3">
          <h6><!-- Insert Job Title Here --> Visual Graphic Design</h6>
          <small class="text-muted"><!-- Company + Dates --> Microcadd • 3 months</small>
          <p class="small">
            <!-- Short description of what you did -->
            We did Logo, Packaging, Store, Poster, Booth design and more.
          </p>
        </div>

        <div class="mt-3">
          <h6>Computer Systems Servicing</h6>
          <small class="text-muted">Mary Grace International • 3 months</small>
          <p class="small">We set up, fix and maintain network and computers. We troubleshoot hardware and software issues. We check cables and Devices to make sure everything runs smoothly.</p>
        </div>
      </div>

      <div class="col-md-6">
        <h4>Education & Skills</h4>

        <p class="mt-3">
          <!-- Insert education -->
          Information Technology- Software Engineer • Trinity University of Asia • 2nd year
        </p>

        <ul class="small">
          <li><!-- Skill 1 --> Computer Systems Servicing NC2</li>
          <li><!-- Skill 2 --> Visual Graphic Design NC3</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- PORTFOLIO SECTION -->
<section id="Certificate" class="py-5">
  <div class="container">
    <h2 class="fw-bold text-center mb-5">Portfolio</h2>

    <div class="row g-4 justify-content-center">

      <!-- Mary Grace -->
      <div class="col-md-4 text-center">
        <div class="p-4 border rounded">
          <h6>Mary Grace International</h6>
          <p class="small">
            (April 1–June 27) Computer Systems Servicing where we install, maintain,
            and repair computer systems and networks.
          </p>
        </div>
      </div>

      <!-- Microcadd -->
      <div class="col-md-4 text-center">
        <div class="p-4 border rounded">
          <h6>Microcadd Institute</h6>
          <p class="small">
            (April–July) Visual Graphic Design where we create visual content
            using images, colors, and typography.
          </p>
        </div>
      </div>

    </div>
  </div>
</section>


<!-- DOG VS CAT GAME SECTION -->
<section id="game" class="py-5">
  <div class="container">
    <h2 class="fw-bold text-center mb-5">Dog vs Cat Game</h2>
    <div style="text-align: center;">
      <div id="loadingStatus" style="font-size: 14px; color: #1e90ff; margin-bottom: 10px;">Loading game...</div>
      <div id="info">
        Score: <span id="score">0</span> |
        Lives: <span id="lives">3</span>
      </div>
      <canvas id="gameCanvas" width="480" height="360" style="background: #222; border: 2px solid #555; border-radius: 8px; display: block; margin: 0 auto 8px;"></canvas>
      <button id="startBtn" disabled style="padding: 6px 14px; border: none; border-radius: 4px; cursor: pointer; background: #1e90ff; color: #fff; font-size: 14px;">Start</button>
      <button id="pauseBtn" disabled style="padding: 6px 14px; border: none; border-radius: 4px; cursor: pointer; background: #1e90ff; color: #fff; font-size: 14px; margin-left: 5px;">Pause</button>
      <button id="restartBtn" disabled style="padding: 6px 14px; border: none; border-radius: 4px; cursor: pointer; background: #1e90ff; color: #fff; font-size: 14px; margin-left: 5px;">Restart</button>
      <div style="margin-top: 10px; display: flex; align-items: center; justify-content: center; gap: 10px;">
        <label for="volumeControl" style="font-size: 12px;">Music Vol:</label>
        <input type="range" id="volumeControl" min="0" max="100" value="50" style="width: 120px;">
        <span id="volumeValue" style="font-size: 12px; min-width: 35px;">50%</span>
      </div>
      <div style="font-size: 12px; opacity: 0.8; margin-top: 6px;">Move: A / D or ← / → • Shoot: SHIFT • Restart: R</div>
    </div>
  </div>
</section>

<!-- CONTACT SECTION -->
<section id="contact" class="py-5 bg-light">
  <div class="container">
    <h2 class="fw-bold text-center mb-4">Contact</h2>


    <div class="row justify-content-center">
      <div class="col-lg-10">
        <div class="row g-4">
          <div class="col-md-4">
            <div class="p-4 bg-white rounded shadow-sm h-100">
              <h5 class="fw-bold">Contact Information</h5>
                <p class="mb-1"><strong>Email:</strong> allexycasandrasteoco@tua.edu.ph</p>
                <p class="mb-1"><strong>Phone:</strong> +1 234 567 890</p>
                <p class="mb-1"><strong>Location:</strong> Quezon City, Philippines</p>
            </div>
          </div>

          <div class="col-md-8">
            <div class="p-4 bg-white rounded shadow-sm h-100">
              <form id="contactForm">
                <div class="mb-3">
                  <label>Name</label>
                  <input id="contactName" name="name" type="text" class="form-control" placeholder="Enter your name" />
                </div>

                <div class="mb-3">
                  <label>Email</label>
                  <input id="contactEmail" name="email" type="email" class="form-control" placeholder="Enter your email" />
                </div>

                <div class="mb-3">
                  <label>Message</label>
                  <textarea id="contactMessage" name="message" class="form-control" rows="4" placeholder="Write any message here"></textarea>
                </div>

                <button type="submit" class="btn btn-primary w-100 btn-pill">Send Message</button>
              </form>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</section>

<footer class="text-center py-3">
  © Allexy Casandra Teoco — All Rights Reserved
</footer>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

<!-- Dog vs Cat Game Script -->
<script>
(function(){
  const canvas = document.getElementById("gameCanvas");
  const ctx = canvas.getContext("2d");
  const scoreEl = document.getElementById("score");
  const livesEl = document.getElementById("lives");
  const restartBtn = document.getElementById("restartBtn");
  const pauseBtn = document.getElementById("pauseBtn");
  const startBtn = document.getElementById("startBtn");
  const volumeControl = document.getElementById("volumeControl");
  const volumeValue = document.getElementById("volumeValue");

  const W = canvas.width;
  const H = canvas.height;

  let player;
  let bullets = [];
  let enemies = [];
  let keys = {};
  let score = 0;
  let lives = 3;
  let gameOver = false;
  let lastTime = 0;
  let spawnTimer = 0;
  let animationId = null;
  let imageReady = false;
  let paused = false;
  let gameStarted = false;

  const enemyImg = new Image();
  enemyImg.src = "cat.png";   

  const boomImg = new Image();
  boomImg.src = "boom.png";

  enemyImg.onload = () => {
    console.log("Alien image loaded!");
    imageReady = true;
    const loadingEl = document.getElementById('loadingStatus');
    if (loadingEl) loadingEl.textContent = 'Ready — click Start to play';
    if (startBtn) startBtn.disabled = false;
  };

  enemyImg.onerror = () => {
    alert("Could not load cat.png. Make sure it is in the same folder and named exactly 'cat.png'.");
  };


const enemySound = new Audio("meow.mp3");
enemySound.volume = 0.07; 

function playEnemySound() {
  if (paused) return; 
  enemySound.currentTime = 0; 
  enemySound.play().catch(()=>{});          
}

const crySound = new Audio('cry.mp3');
crySound.volume = 0.9;
let cryPlayed = false;
function playCry(){
  if(cryPlayed) return;
  cryPlayed = true;
  try{
    crySound.currentTime = 0;
    crySound.play().catch(()=>{});
    setTimeout(()=>{ try{ crySound.pause(); crySound.currentTime = 0; }catch(e){} }, 3000);
  }catch(e){}
}


volumeControl.addEventListener("input", (e) => {
  const volumePercent = e.target.value;
  const v = Math.min(Math.max(volumePercent / 100, 0), 1); 
  
  if (typeof backgroundSound !== 'undefined') backgroundSound.volume = v;
  volumeValue.textContent = volumePercent + "%";
});


const backgroundSound = new Audio("sound.mp3");
backgroundSound.preload = 'auto';
backgroundSound.volume = 0.5; 
backgroundSound.loop = true;

function playBackgroundSound() {
  backgroundSound.currentTime = 0;
  backgroundSound.play().then(() => {
    console.log('Background music playing');
  }).catch((err) => {
    console.warn('Background play() rejected:', err);
  });
}


let backgroundStarted = false;
function tryStartBackground() {
  if (backgroundStarted) return;
  backgroundSound.play().then(() => { backgroundStarted = true; }).catch(()=>{});
}
 
  let playerImgReady = false;
  const playerImg = new Image();
  playerImg.src = "player.png";   
  playerImg.onload = () => {
    console.log("Player image loaded!");
    playerImgReady = true;
  };

  function createPlayer() {
    return {
      w: 60,
      h: 40,
      x: W / 2 - 60,
      y: H - 40,
      speed: 0.30   
    };
  }

  function spawnEnemy() {
    const size = 50;            
    const x = Math.random() * (W - size);
    const y = -size;
    const speed = 0.05 + Math.random() * 0.06;

    enemies.push({ x, y, w: size, h: size, speed, state: 'alive' });
  }

  function shootBullet() {
    bullets.push({
      x: player.x + player.w / 2 - 3,
      y: player.y,
      w: 6,
      h: 14,
      speed: 0.6
    });
  }

  function resetGame() {
    if (!imageReady) return;  
    player = createPlayer();
    bullets = [];
    enemies = [];
    score = 0;
    lives = 3;
    gameOver = false;
    backgroundStarted = false;
    try{ backgroundSound.pause(); backgroundSound.currentTime = 0; }catch(e){}
    try{ enemySound.pause(); enemySound.currentTime = 0; }catch(e){}
    scoreEl.textContent = score;
    livesEl.textContent = lives;
    lastTime = performance.now();
    spawnTimer = 0;
    if (animationId) cancelAnimationFrame(animationId);
    paused = false;
    if(pauseBtn) { pauseBtn.textContent = 'Pause'; pauseBtn.disabled = false; }
    if(restartBtn) restartBtn.disabled = false;
    gameStarted = true;
    // restart background music
    tryStartBackground();
    animationId = requestAnimationFrame(gameLoop);
  }

  function handleInput(delta) {
    const distance = player.speed * delta;
    if (keys["ArrowLeft"] || keys["a"]) player.x -= distance;
    if (keys["ArrowRight"] || keys["d"]) player.x += distance;

    if (player.x < 0) player.x = 0;
    if (player.x + player.w > W) player.x = W - player.w;
  }

  function updateBullets(delta) {
    bullets.forEach(b => b.y -= b.speed * delta);
    bullets = bullets.filter(b => b.y + b.h > 0);
  }

  function updateEnemies(delta) {
    enemies.forEach(e => {
      if (e.state === 'alive') {
        e.y += e.speed * delta;
      } else if (e.state === 'boom') {
        e.explosionTimer -= delta;
      }
    });

    enemies = enemies.filter(e => {
      if (e.state === 'alive') {
        if (e.y > H) {
          lives--;
          livesEl.textContent = lives;
          if (lives <= 0) {
            gameOver = true;
            try{ backgroundSound.pause(); backgroundSound.currentTime = 0; }catch(e){}
            try{ enemySound.pause(); enemySound.currentTime = 0; }catch(e){}
            playCry();
          }
          return false;
        }
        return true;
      }

      if (e.state === 'boom') {
        return e.explosionTimer > 0;
      }

      return true;
    });
  }

  function checkCollision(a, b) {
    return !(
      a.x + a.w < b.x ||
      a.x > b.x + b.w ||
      a.y + a.h < b.y ||
      a.y > b.y + b.h
    );
  }

  function handleCollisions() {
    for (let i = enemies.length - 1; i >= 0; i--) {
      for (let j = bullets.length - 1; j >= 0; j--) {
        if (checkCollision(enemies[i], bullets[j])) {
          if (enemies[i].state !== 'boom') {
            enemies[i].state = 'boom';
            enemies[i].explosionTimer = 400; 
            enemies[i].speed = 0;
            playEnemySound();
            score += 10;
            scoreEl.textContent = score;
          }
          bullets.splice(j, 1);
          break;
        }
      }
    }

    for (const e of enemies) {
      if (checkCollision(e, player)) {
        lives = 0;
        livesEl.textContent = lives;
        gameOver = true;
        try{ backgroundSound.pause(); backgroundSound.currentTime = 0; }catch(ex){}
        try{ enemySound.pause(); enemySound.currentTime = 0; }catch(ex){}
        playCry();
        break;
      }
    }
  }

  function drawAlienFallback(x, y, w, h) {
    ctx.fillStyle = "#00ff00";
    ctx.beginPath();
    ctx.ellipse(x + w / 2, y + h / 3, w / 3, h / 4, 0, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.beginPath();
    ctx.ellipse(x + w / 2, y + (h * 2 / 3), w / 2, h / 3, 0, 0, Math.PI * 2);
    ctx.fill();
    
    ctx.fillStyle = "white";
    ctx.beginPath();
    ctx.arc(x + w / 3, y + h / 3, 4, 0, Math.PI * 2);
    ctx.fill();
    ctx.beginPath();
    ctx.arc(x + (w * 2 / 3), y + h / 3, 4, 0, Math.PI * 2);
    ctx.fill();
  }

  function draw() {
    ctx.clearRect(0, 0, W, H);

    if (playerImgReady) {
      ctx.drawImage(playerImg, player.x, player.y, player.w, player.h);
    } else {
      ctx.fillStyle = "#1e90ff";
      ctx.fillRect(player.x, player.y, player.w, player.h);
      ctx.fillStyle = "#87cefa";
      ctx.fillRect(player.x + player.w / 2 - 4, player.y - 10, 8, 10);
    }

    ctx.fillStyle = "yellow";
    bullets.forEach(b => ctx.fillRect(b.x, b.y, b.w, b.h));

    enemies.forEach(e => {
      if (e.state === 'boom') {
        if (boomImg && boomImg.complete) {
          ctx.drawImage(boomImg, e.x, e.y, e.w, e.h);
        } else {
          ctx.fillStyle = "orange";
          ctx.fillRect(e.x, e.y, e.w, e.h);
        }
      } else {
        if (imageReady) {
          ctx.drawImage(enemyImg, e.x, e.y, e.w, e.h);
        } else {
          ctx.fillStyle = "red";
          ctx.fillRect(e.x, e.y, e.w, e.h);
        }
      }
    });

    if (gameOver) {
      ctx.fillStyle = "rgba(0,0,0,0.6)";
      ctx.fillRect(0, H / 2 - 40, W, 80);
      ctx.fillStyle = "#fff";
      ctx.font = "26px Arial";
      ctx.textAlign = "center";
      ctx.fillText("GAME OVER", W / 2, H / 2 - 4);
      ctx.font = "16px Arial";
      ctx.fillText("Press R or click Restart", W / 2, H / 2 + 22);
      ctx.textAlign = "start";
    }
  }

  function gameLoop(timestamp) {
    const delta = timestamp - lastTime;
    lastTime = timestamp;
    if (!gameOver && !paused) {
      handleInput(delta);
      updateBullets(delta);
      updateEnemies(delta);

      spawnTimer += delta;
      const spawnInterval = Math.max(400, 1000 - score * 2);
      if (spawnTimer > spawnInterval) {
        spawnEnemy();
        spawnTimer = 0;
      }

      handleCollisions();
    }

    draw();

    if (!gameOver && !paused) {
      animationId = requestAnimationFrame(gameLoop);
    }
  }

  // Controls
  window.addEventListener("keydown", e => {
    keys[e.key] = true;
    if (e.key === "Shift" && !gameOver && imageReady && !paused && gameStarted) {
      shootBullet();
    }
    if ((e.key === "r" || e.key === "R") && gameOver) {
      resetGame();
    }
  });

  window.addEventListener("keyup", e => {
    keys[e.key] = false;
  });

  restartBtn.addEventListener("click", resetGame);

  if (pauseBtn) {
    pauseBtn.addEventListener('click', ()=>{
      if (gameOver) return;
      if (!paused) {
        // pause
        paused = true;
        if (animationId) cancelAnimationFrame(animationId);
        try{ backgroundSound.pause(); }catch(e){}
        try{ enemySound.pause(); }catch(e){}
        try{ enemySound.currentTime = 0; }catch(e){}
        pauseBtn.textContent = 'Resume';
      } else {
        paused = false;
        lastTime = performance.now();
        backgroundSound.play().then(()=>{ backgroundStarted = true; }).catch(()=>{});
        animationId = requestAnimationFrame(gameLoop);
        pauseBtn.textContent = 'Pause';
      }
    });
  }

  if (startBtn) {
    startBtn.addEventListener('click', ()=>{
      if (!imageReady) return;
      resetGame();
      startBtn.disabled = true;
      if (pauseBtn) pauseBtn.disabled = false;
      if (restartBtn) restartBtn.disabled = false;
    });
  }
})();
</script>

</body>
</html>
