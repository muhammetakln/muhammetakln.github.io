<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Muhammet Akalın | Portfolio</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
--bg-color: #0d1117;
--card-bg: #161b22;
--border-color: #30363d;
--text-main: #c9d1d9;
--text-muted: #8b949e;
--accent-color: #58a6ff;
--accent-glow: rgba(88, 166, 255, 0.15);
--success-color: #2ea44f;
}

* {
margin: 0;
padding: 0;
box-sizing: border-box;
font-family: 'Inter', sans-serif;
scroll-behavior: smooth;
}

body {
background-color: var(--bg-color);
color: var(--text-main);
line-height: 1.6;
overflow-x: hidden;
}

.container {
max-width: 1100px;
margin: 0 auto;
padding: 2rem;
}

header {
display: flex;
justify-content: space-between;
align-items: center;
padding: 1.5rem 0;
border-bottom: 1px solid var(--border-color);
margin-bottom: 3rem;
}

.logo {
font-weight: 700;
font-size: 1.2rem;
color: #fff;
text-decoration: none;
display: flex;
align-items: center;
gap: 0.5rem;
}

.logo span {
color: var(--accent-color);
}

nav .nav-links {
display: flex;
gap: 1.5rem;
list-style: none;
}

nav .nav-links a {
color: var(--text-muted);
text-decoration: none;
font-size: 0.95rem;
transition: color 0.3s;
}

nav .nav-links a:hover {
color: var(--accent-color);
}

.hero {
display: flex;
align-items: center;
gap: 3rem;
margin-bottom: 5rem;
padding: 2rem 0;
}

.hero-content {
flex: 1;
}

.hero-badge {
background: var(--accent-glow);
color: var(--accent-color);
padding: 0.4rem 1rem;
border-radius: 2rem;
font-size: 0.85rem;
font-weight: 600;
display: inline-block;
margin-bottom: 1rem;
border: 1px solid rgba(88, 166, 255, 0.3);
}

.hero h1 {
font-size: 3rem;
color: #fff;
margin-bottom: 1rem;
font-weight: 700;
letter-spacing: -0.05rem;
}

.hero p {
font-size: 1.1rem;
color: var(--text-muted);
margin-bottom: 2rem;
max-width: 600px;
}

.hero-avatar img {
width: 220px;
height: 220px;
border-radius: 50%;
border: 4px solid var(--border-color);
box-shadow: 0 10px 30px rgba(0,0,0,0.5);
transition: transform 0.3s ease;
}

.hero-avatar img:hover {
transform: scale(1.03);
border-color: var(--accent-color);
}

.btn-group {
display: flex;
gap: 1rem;
}

.btn {
display: inline-flex;
align-items: center;
gap: 0.5rem;
padding: 0.75rem 1.5rem;
border-radius: 6px;
font-size: 0.95rem;
font-weight: 500;
text-decoration: none;
transition: all 0.3s;
cursor: pointer;
border: 1px solid transparent;
}

.btn-primary {
background-color: var(--success-color);
color: #fff;
}

.btn-primary:hover {
background-color: #2c974b;
}

.btn-secondary {
background-color: var(--card-bg);
color: var(--text-main);
border: 1px solid var(--border-color);
}

.btn-secondary:hover {
background-color: #21262d;
border-color: var(--text-muted);
}

.section-title {
font-size: 1.75rem;
color: #fff;
margin-bottom: 2rem;
display: flex;
align-items: center;
gap: 0.75rem;
border-bottom: 1px solid var(--border-color);
padding-bottom: 0.75rem;
}

.skills-section {
margin-bottom: 5rem;
}

.skills-grid {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
gap: 1.25rem;
}

.skill-card {
background: var(--card-bg);
border: 1px solid var(--border-color);
border-radius: 6px;
padding: 1.2rem;
text-align: center;
transition: all 0.3s;
}

.skill-card:hover {
transform: translateY(-3px);
border-color: var(--accent-color);
box-shadow: 0 4px 20px var(--accent-glow);
}

.skill-card i {
font-size: 2rem;
margin-bottom: 0.75rem;
}

.skill-card.dotnet i { color: #512bd4; }
.skill-card.csharp i { color: #239120; }
.skill-card.sql i { color: #00758f; }
.skill-card.docker i { color: #2496ed; }
.skill-card.web i { color: #f0db4f; }

.skill-card h3 {
font-size: 1rem;
color: #fff;
}

.projects-section {
margin-bottom: 5rem;
}

.projects-grid {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(48%, 1fr));
gap: 2rem;
}

.project-card {
background: var(--card-bg);
border: 1px solid var(--border-color);
border-radius: 8px;
padding: 1.75rem;
display: flex;
flex-direction: column;
justify-content: space-between;
transition: all 0.3s;
}

.project-card:hover {
border-color: #8b949e;
transform: translateY(-4px);
box-shadow: 0 8px 24px rgba(0,0,0,0.3);
}

.project-top {
display: flex;
justify-content: space-between;
align-items: flex-start;
margin-bottom: 1rem;
}

.folder-icon {
font-size: 1.5rem;
color: var(--text-muted);
}

.project-links a {
color: var(--text-muted);
font-size: 1.2rem;
margin-left: 0.75rem;
transition: color 0.3s;
text-decoration: none;
}

.project-links a:hover {
color: var(--accent-color);
}

.project-card h3 {
font-size: 1.3rem;
color: #fff;
margin-bottom: 0.75rem;
}

.project-card h3 a {
color: inherit;
text-decoration: none;
}

.project-card h3 a:hover {
color: var(--accent-color);
}

.project-card p {
color: var(--text-muted);
font-size: 0.95rem;
margin-bottom: 1.5rem;
flex-grow: 1;
}

.project-tech {
display: flex;
gap: 0.75rem;
flex-wrap: wrap;
}

.tech-tag {
font-size: 0.8rem;
color: var(--accent-color);
background: rgba(88, 166, 255, 0.1);
padding: 0.2rem 0.6rem;
border-radius: 2rem;
font-weight: 500;
}

footer {
border-top: 1px solid var(--border-color);
padding: 2rem 0;
text-align: center;
color: var(--text-muted);
font-size: 0.9rem;
}

footer a {
color: var(--text-main);
text-decoration: none;
}

footer a:hover {
color: var(--accent-color);
}

@media (max-width: 768px) {
.projects-grid { grid-template-columns: 1fr; }
.hero { flex-direction: column-reverse; text-align: center; gap: 2rem; }
.hero p { margin: 0 auto 2rem auto; }
.btn-group { justify-content: center; }
.hero h1 { font-size: 2rem; }
}
</style>
</head>
<body>
<div class="container">
<header>
<a href="#" class="logo"><i class="fab fa-github"></i> muhammetakln<span>.io</span></a>
<nav>
<ul class="nav-links">
<li><a href="#about">Hakkımda</a></li>
<li><a href="#skills">Yetenekler</a></li>
<li><a href="#projects">Projeler</a></li>
</ul>
</nav>
</header>

<section class="hero" id="about">
<div class="hero-content">
<span class="hero-badge">Full-Stack Developer</span>
<h1>Merhaba, Ben Muhammet</h1>
<p>.NET ekosistemi, modern web teknolojileri ve mimari tasarımlar üzerine odaklanmış bir yazılım geliştiriciyim. Performanslı, ölçeklenebilir ve temiz kod prensiplerine uygun projeler üretiyorum.</p>
<div class="btn-group">
<a href="https://github.com/muhammetakln" target="_blank" class="btn btn-primary"><i class="fab fa-github"></i> GitHub Profilim</a>
<a href="#projects" class="btn btn-secondary">Projelerimi Gör</a>
</div>
</div>
<div class="hero-avatar">
<img src="https://avatars.githubusercontent.com/muhammetakln" alt="Muhammet Akalın">
</div>
</section>

<section class="skills-section" id="skills">
<h2 class="section-title"><i class="fas fa-code"></i> Teknolojik Yetkinlikler</h2>
<div class="skills-grid">
<div class="skill-card dotnet"><i class="fab fa-microsoft"></i><h3>ASP.NET Core</h3></div>
<div class="skill-card csharp"><i class="fas fa-hashtag"></i><h3>C# / EF Core</h3></div>
<div class="skill-card sql"><i class="fas fa-database"></i><h3>SQL / SQLite</h3></div>
<div class="skill-card docker"><i class="fab fa-docker"></i><h3>Docker & DevOps</h3></div>
<div class="skill-card web"><i class="fas fa-laptop-code"></i><h3>Web Geliştirme</h3></div>
</div>
</section>

<section class="projects-section" id="projects">
<h2 class="section-title"><i class="fas fa-cubes"></i> Öne Çıkan Projeler</h2>
<div class="projects-grid">
<div class="project-card">
<div class="project-top">
<i class="far fa-folder folder-icon"></i>
<div class="project-links"><a href="https://github.com/muhammetakln" target="_blank"><i class="fab fa-github"></i></a></div>
</div>
<div>
<h3><a href="https://github.com/muhammetakln" target="_blank">StayHub</a></h3>
<p>Otel rezervasyon süreçlerini uçtan uca yöneten kapsamlı bir otomasyon sistemi. Oda yönetimi, rezervasyon mantığı ve kullanıcı değerlendirme modüllerini barındıran mimari odaklı bir mezuniyet projesi.</p>
</div>
<div class="project-tech">
<span class="tech-tag">C#</span><span class="tech-tag">ASP.NET Core</span><span class="tech-tag">EF Core</span><span class="tech-tag">Docker</span>
</div>
</div>

<div class="project-card">
<div class="project-top">
<i class="far fa-folder folder-icon"></i>
<div class="project-links"><a href="https://github.com/muhammetakln/ECommerce" target="_blank"><i class="fab fa-github"></i></a></div>
</div>
<div>
<h3><a href="https://github.com/muhammetakln/ECommerce" target="_blank">ECommerce</a></h3>
<p>Katmanlı mimari (Layered Architecture) ve kurumsal tasarım kalıpları (Unit of Work, Repository vb.) kullanılarak geliştirilmiş modern, optimize ve güvenli bir e-ticaret arka plan altyapısı.</p>
</div>
<div class="project-tech">
<span class="tech-tag">.NET Core</span><span class="tech-tag">Web API</span><span class="tech-tag">MSSQL</span><span class="tech-tag">Repository Pattern</span>
</div>
</div>
</div>
</section>

<footer>
<p>&copy; 2026 Muhammet Akalın. Tüm Hakları Saklıdır.</p>
<p style="margin-top: 0.5rem; font-size: 0.8rem;">Bu sayfa <a href="https://pages.github.com" target="_blank">GitHub Pages</a> ile barındırılmaktadır.</p>
</footer>
</div>
</body>
</html>
