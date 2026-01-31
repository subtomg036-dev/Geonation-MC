<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Geonation Minecraft Server</title>
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Press Start 2P', cursive;
      background: linear-gradient(135deg, #0b3d0b, #000);
      color: #fff;
      min-height: 100vh;
    }
    a { color: white; text-decoration: none; }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px;
    }

    .logo {
      font-size: 20px;
      cursor: pointer;
    }

    .vip-btn {
      margin-left: 15px;
      padding: 10px 16px;
      border-radius: 20px;
      background: #1faa1f;
      color: #000;
      font-size: 12px;
      cursor: pointer;
    }

    .socials img {
      width: 32px;
      margin-left: 10px;
      cursor: pointer;
    }

    .page {
      display: none;
      text-align: center;
      padding: 80px 20px;
    }

    .page.active {
      display: block;
    }

    h1 {
      font-size: 48px;
      margin-bottom: 60px;
      text-shadow: 4px 4px #000;
    }

    .server-info {
      margin-top: 120px;
      font-size: 14px;
      line-height: 2.2;
    }

    .status {
      color: #00ff00;
    }

    /* VIP PAGE */
    .ranks {
      display: flex;
      justify-content: center;
      gap: 40px;
      flex-wrap: wrap;
      margin-top: 80px;
    }

    .rank-box {
      background: rgba(0,0,0,0.6);
      border: 2px solid #1faa1f;
      border-radius: 20px;
      width: 220px;
      padding: 30px 20px;
    }

    .rank-box h2 {
      margin-bottom: 20px;
      color: #1faa1f;
    }

    .price {
      font-size: 14px;
    }
  </style>
</head>
<body>

<header>
  <div>
    <span class="logo" onclick="showPage('home')">Geonation</span>
    <button class="vip-btn" onclick="showPage('vip')">VIP Ranks</button>
  </div>

  <div class="socials">
    <a href="https://www.tiktok.com/@mc_itzzmg" target="_blank">
      <img src="https://upload.wikimedia.org/wikipedia/commons/0/08/TikTok_logo.svg" alt="TikTok" />
    </a>
    <a href="https://discord.gg/tcvtMVpj" target="_blank">
      <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/discord.svg" alt="Discord" />
    </a>
  </div>
</header>

<!-- HOME PAGE -->
<section id="home" class="page active">
  <h1>Geonation</h1>

  <div class="server-info">
    <p>Server Name: Geonation</p>
    <p>IP: 91.197.6.16:22976</p>
    <p>Status: <span class="status">ONLINE 24/7</span></p>
  </div>
</section>

<!-- VIP PAGE -->
<section id="vip" class="page">
  <h1>VIP Ranks</h1>

  <div class="ranks">
    <div class="rank-box">
      <h2>VIP</h2>
      <p class="price">Price: 10 GEL</p>
    </div>

    <div class="rank-box">
      <h2>+VIP</h2>
      <p class="price">Price: 20 GEL</p>
    </div>
  </div>
</section>

<script>
  function showPage(pageId) {
    document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
    document.getElementById(pageId).classList.add('active');
  }
</script>

</body>
</html>
