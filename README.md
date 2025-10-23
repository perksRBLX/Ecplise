<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Eclipse Admin Panel</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
:root {
  --bg:#0b0b0b; 
  --panel:#0f0f13; 
  --accent:#00e0ff; 
  --accent2:#33cfff; 
  --muted:#9aa0a6; 
  --radius:12px; 
  --gap:28px;
}
*{box-sizing:border-box;}
html,body{
  height:100%;margin:0;
  font-family:Inter,system-ui,Segoe UI,Roboto,Arial;
  background:linear-gradient(180deg,#050505 0%, #0c0c0c 100%);
  color:#e9eef2;
}
a{color:inherit;text-decoration:none;}
header{
  display:flex;align-items:center;justify-content:space-between;
  padding:18px 24px;gap:12px;
  background:rgba(255,255,255,0.02);
  border-bottom:1px solid rgba(255,255,255,0.05);
  backdrop-filter:blur(8px);
  position:sticky;top:0;z-index:100;
}
.brand{display:flex;align-items:center;gap:12px;}
.logo{
  width:52px;height:52px;display:flex;
  align-items:center;justify-content:center;
}
.logo img{width:100%;height:auto;}
.title{font-weight:800;font-size:1.15rem;}
nav{display:flex;gap:12px;}
nav a{
  padding:8px 12px;border-radius:8px;
  color:var(--muted);font-size:0.95rem;
  transition:0.2s;
}
nav a:hover{color:var(--accent);}
nav a.cta{
  background:linear-gradient(90deg,var(--accent),var(--accent2));
  color:#fff;font-weight:600;
}
.container{max-width:1100px;margin:18px auto;padding:0 18px;}
.hero{
  display:grid;grid-template-columns:1fr 420px;gap:24px;align-items:center;margin-top:24px;
}
.card{
  background:var(--panel);
  border-radius:var(--radius);
  padding:22px;
  box-shadow:0 6px 22px rgba(0,0,0,0.6);
}
.hero .left h1{margin:0 0 10px;font-size:2.05rem;}
.meta{color:var(--muted);margin-bottom:14px;}
.btn{
  background:rgba(255,255,255,0.03);
  border:1px solid rgba(255,255,255,0.08);
  padding:10px 14px;border-radius:10px;
  color:#e9eef2;font-weight:600;cursor:pointer;
  transition:0.2s;
}
.btn:hover{background:rgba(255,255,255,0.08);}
.btn.primary{
  background:linear-gradient(90deg,var(--accent),var(--accent2));
  border:none;
}
.ip{
  font-family:monospace;
  background:rgba(0,0,0,0.25);
  padding:8px 10px;border-radius:8px;
}
#viewerWrap{
  height:360px;border-radius:12px;overflow:hidden;
  display:flex;align-items:center;justify-content:center;
  background:linear-gradient(180deg,#0b0b0b,#071018);
}
#viewerWrap img{
  width:200px;height:auto;filter:drop-shadow(0 0 20px rgba(0,224,255,0.4));
}
.grid3{
  display:grid;grid-template-columns:repeat(3,1fr);
  gap:14px;margin-top:18px;
}
.muted{color:var(--muted);font-size:0.92rem;}
footer{
  margin:40px 0 60px;text-align:center;
  color:var(--muted);font-size:0.9rem;
  border-top:1px solid rgba(255,255,255,0.05);
  padding-top:18px;
}
@media (max-width:980px){
  .hero{grid-template-columns:1fr;}
  #viewerWrap{height:280px}
  .grid3{grid-template-columns:1fr}
}
</style>
</head>
<body>

<header class="container">
  <div class="brand">
    <div class="logo">
      <img src="https://i.imgur.com/09KdqWl.png" alt="Eclipse Admin Panel Logo">
    </div>
    <div>
      <div class="title">Eclipse Admin Panel</div>
      <div class="muted" style="font-size:0.82rem">Roblox • Admin & Moderation</div>
    </div>
  </div>
  <nav>
    <a href="#home">Home</a>
    <a href="#features">Features</a>
    <a href="#status">Status</a>
    <a class="cta" href="#release">Coming Soon</a>
  </nav>
</header>

<main class="container" id="home">
  <section class="hero">
    <div class="card left">
      <h1>Eclipse Admin Panel — Coming Soon</h1>
      <p class="meta">A fast, elegant, and powerful admin panel for Roblox. Manage servers, run commands, and moderate with ease.</p>
      <div style="display:flex;gap:14px;align-items:center;flex-wrap:wrap">
        <div class="ip card" style="display:flex;align-items:center;gap:10px">
          <div style="min-width:72px">Status:</div>
          <div style="font-weight:700" id="serverStatus">Alpha Development</div>
        </div>
        <div class="controls">
          <button class="btn primary" id="joinBtn">Learn More</button>
        </div>
      </div>
    </div>

    <div class="card" id="viewerWrap">
      <img src="https://i.imgur.com/09KdqWl.png" alt="Eclipse Logo">
    </div>
  </section>

  <section id="features" style="margin-top:18px">
    <div class="card">
      <h2>Features (Planned)</h2>
      <ul class="muted">
        <li>Advanced anticheat system</li>
        <li>Filtering and moderation tools</li>
        <li>Clean, intuitive command UI</li>
        <li>Constant updates for stability and performance</li>
      </ul>
    </div>
  </section>

  <section id="status" style="margin-top:18px">
    <div class="card">
      <h2>Status</h2>
      <p class="muted">Eclipse is currently in Alpha development. Expect updates, new features, and bug fixes in every release.</p>
    </div>
  </section>

  <section id="release" style="margin-top:18px">
    <div class="card">
      <h2>Release</h2>
      <p class="muted">The first Alpha version is coming soon. Stay tuned for announcements.</p>
    </div>
  </section>
</main>

<footer>
  <div>© 2025 Eclipse Admin Panel — Eclipse Networks</div>
</footer>

</body>
</html>
