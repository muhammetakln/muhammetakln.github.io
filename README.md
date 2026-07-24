<!DOCTYPE html>
<html lang="tr" id="html-root">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muhammet Akalın | Full Stack & .NET Developer</title>
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;700&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-color: #0b0f19;
            --card-bg: #131c2e;
            --card-border: #1e293b;
            --text-main: #f8fafc;
            --text-muted: #94a3b8;
            --accent-cyan: #06b6d4;
            --accent-green: #10b981;
            --accent-purple: #8b5cf6;
            --code-bg: #0f172a;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.7;
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* Ambient Glow Effects */
        .glow-orb {
            position: absolute;
            width: 400px;
            height: 400px;
            background: radial-gradient(circle, rgba(6, 182, 212, 0.15) 0%, rgba(139, 92, 246, 0.05) 50%, transparent 70%);
            z-index: -1;
            border-radius: 50%;
            filter: blur(60px);
        }

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: rgba(11, 15, 25, 0.85);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid var(--card-border);
            z-index: 1000;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1.2rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Fira Code', monospace;
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--accent-cyan);
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .logo span {
            color: var(--accent-green);
        }

        .nav-right {
            display: flex;
            align-items: center;
            gap: 2.5rem;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            font-size: 0.95rem;
            font-weight: 500;
            color: var(--text-muted);
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--accent-cyan);
        }

        .lang-switch {
            background: linear-gradient(135deg, rgba(6, 182, 212, 0.1), rgba(16, 185, 129, 0.1));
            border: 1px solid var(--accent-cyan);
            color: var(--accent-cyan);
            padding: 0.4rem 1rem;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            font-size: 0.85rem;
            font-family: 'Fira Code', monospace;
            transition: all 0.3s ease;
        }

        .lang-switch:hover {
            background: var(--accent-cyan);
            color: var(--bg-color);
            box-shadow: 0 0 15px rgba(6, 182, 212, 0.4);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        section {
            padding: 7rem 0 4rem 0;
        }

        /* Hero Section */
        #hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 3rem;
            position: relative;
        }

        .hero-content {
            flex: 1;
        }

        .terminal-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            background-color: var(--code-bg);
            border: 1px solid var(--card-border);
            padding: 0.5rem 1rem;
            border-radius: 8px;
            font-family: 'Fira Code', monospace;
            font-size: 0.85rem;
            color: var(--accent-green);
            margin-bottom: 1.5rem;
            box-shadow: 0 4px 20px rgba(0,0,0,0.3);
        }

        .terminal-badge .dot {
            width: 8px;
            height: 8px;
            background-color: var(--accent-green);
            border-radius: 50%;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.3); opacity: 0.4; }
            100% { transform: scale(1); opacity: 1; }
        }

        .hero-content h1 {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 0.5rem;
            letter-spacing: -0.02em;
            background: linear-gradient(to right, #fff, var(--text-muted));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-content h2 {
            font-family: 'Fira Code', monospace;
            font-size: 1.4rem;
            color: var(--accent-cyan);
            font-weight: 600;
            margin-bottom: 1.5rem;
        }

        .hero-content p {
            font-size: 1.1rem;
            color: var(--text-muted);
            max-width: 600px;
            margin-bottom: 2.5rem;
        }

        .btn-group {
            display: flex;
            gap: 1.2rem;
        }

        .btn {
            padding: 0.85rem 1.8rem;
            border-radius: 8px;
            font-weight: 600;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            font-size: 0.95rem;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--accent-cyan), #0284c7);
            color: #0b0f19;
            box-shadow: 0 4px 20px rgba(6, 182, 212, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 25px rgba(6, 182, 212, 0.5);
        }

        .btn-outline {
            border: 1px solid var(--card-border);
            background-color: var(--card-bg);
            color: var(--text-main);
        }

        .btn-outline:hover {
            border-color: var(--accent-purple);
            color: var(--accent-purple);
            transform: translateY(-2px);
        }

        /* Hero Code Card */
        .hero-visual {
            flex: 1;
            display: flex;
            justify-content: flex-end;
        }

        .code-window {
            background-color: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            width: 100%;
            max-width: 500px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.5);
            overflow: hidden;
        }

        .code-header {
            background-color: var(--code-bg);
            padding: 0.8rem 1.2rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            border-bottom: 1px solid var(--card-border);
        }

        .code-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .dot-red { background-color: #ef4444; }
        .dot-yellow { background-color: #f59e0b; }
        .dot-green { background-color: #10b981; }

        .code-title {
            margin-left: auto;
            margin-right: auto;
            font-family: 'Fira Code', monospace;
            font-size: 0.8rem;
            color: var(--text-muted);
        }

        .code-body {
            padding: 1.5rem;
            font-family: 'Fira Code', monospace;
            font-size: 0.9rem;
            line-height: 1.6;
            color: #e2e8f0;
        }

        .code-keyword { color: #f472b6; }
        .code-class { color: #38bdf8; }
        .code-string { color: #34d399; }
        .code-variable { color: #fbbf24; }

        /* Section Titles */
        .section-title {
            font-size: 2.2rem;
            font-weight: 800;
            margin-bottom: 3rem;
            color: #ffffff;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .section-title span {
            font-family: 'Fira Code', monospace;
            color: var(--accent-cyan);
            font-size: 1.5rem;
        }

        /* About Section */
        .about-card {
            background-color: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 16px;
            padding: 2.5rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            position: relative;
            overflow: hidden;
        }

        .about-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 4px;
            height: 100%;
            background: linear-gradient(to bottom, var(--accent-cyan), var(--accent-purple));
        }

        .about-card p {
            color: var(--text-muted);
            font-size: 1.15rem;
            margin-bottom: 1.2rem;
        }

        .about-card p:last-child {
            margin-bottom: 0;
        }

        /* Projects Grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 16px;
            padding: 2rem;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
        }

        .project-card:hover {
            transform: translateY(-8px);
            border-color: var(--accent-cyan);
            box-shadow: 0 20px 40px rgba(6, 182, 212, 0.15);
        }

        .project-card h3 {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 1rem;
            color: #ffffff;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .project-card h3 i {
            color: var(--accent-cyan);
            font-size: 1.2rem;
        }

        .project-card p {
            color: var(--text-muted);
            font-size: 1rem;
            margin-bottom: 1.5rem;
        }

        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
            margin-bottom: 2rem;
        }

        .tech-tag {
            background-color: rgba(6, 182, 212, 0.1);
            color: var(--accent-cyan);
            font-family: 'Fira Code', monospace;
            font-size: 0.8rem;
            padding: 0.3rem 0.8rem;
            border-radius: 6px;
            border: 1px solid rgba(6, 182, 212, 0.2);
        }

        .project-links {
            display: flex;
            gap: 1.2rem;
            padding-top: 1rem;
            border-top: 1px solid var(--card-border);
        }

        .project-links a {
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--text-main);
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: color 0.3s ease;
        }

        .project-links a:hover {
            color: var(--accent-cyan);
        }

        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .skill-category {
            background-color: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 16px;
            padding: 2rem;
            transition: transform 0.3s ease;
        }

        .skill-category:hover {
            transform: translateY(-5px);
        }

        .skill-category h4 {
            color: var(--accent-cyan);
            font-family: 'Fira Code', monospace;
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 0.8rem;
        }

        .skill-list {
            list-style: none;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .skill-list li {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            color: var(--text-main);
            font-weight: 500;
            background: var(--code-bg);
            padding: 0.8rem 1rem;
            border-radius: 8px;
            border: 1px solid var(--card-border);
        }

        .skill-list li i {
            color: var(--accent-green);
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .contact-item {
            background-color: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 16px;
            padding: 2rem;
            display: flex;
            align-items: center;
            gap: 1.5rem;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            border-color: var(--accent-cyan);
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(6, 182, 212, 0.1);
        }

        .contact-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, rgba(6, 182, 212, 0.1), rgba(139, 92, 246, 0.1));
            border: 1px solid var(--accent-cyan);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: var(--accent-cyan);
        }

        .contact-info span {
            display: block;
            font-size: 0.85rem;
            color: var(--text-muted);
            font-family: 'Fira Code', monospace;
            margin-bottom: 0.3rem;
        }

        .contact-info a {
            font-size: 1.05rem;
            font-weight: 600;
            color: var(--text-main);
            word-break: break-all;
            transition: color 0.3s ease;
        }

        .contact-info a:hover {
            color: var(--accent-cyan);
        }

        /* Footer */
        footer {
            border-top: 1px solid var(--card-border);
            padding: 3rem 0;
            text-align: center;
            color: var(--text-muted);
            font-family: 'Fira Code', monospace;
            font-size: 0.9rem;
            margin-top: 6rem;
            background-color: rgba(11, 15, 25, 0.5);
        }

        /* Responsive */
        @media (max-width: 968px) {
            #hero {
                flex-direction: column;
                text-align: center;
                padding-top: 4rem;
            }
            .hero-content p {
                margin-left: auto;
                margin-right: auto;
            }
            .btn-group {
                justify-content: center;
            }
            .hero-visual {
                justify-content: center;
                width: 100%;
            }
            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>

    <div class="glow-orb" style="top: 10%; left: 5%;"></div>
    <div class="glow-orb" style="bottom: 20%; right: 5%;"></div>

    <header>
        <div class="nav-container">
            <a href="#hero" class="logo"><i class="fa-solid fa-code"></i> Muhammet<span>.dev</span></a>
            <div class="nav-right">
                <ul class="nav-links">
                    <li><a href="#about" data-tr="Hakkımda" data-en="About Me">Hakkımda</a></li>
                    <li><a href="#projects" data-tr="Projeler" data-en="Projects">Projeler</a></li>
                    <li><a href="#skills" data-tr="Yetenekler" data-en="Skills">Yetenekler</a></li>
                    <li><a href="#contact" data-tr="İletişim" data-en="Contact">İletişim</a></li>
                </ul>
                <button class="lang-switch" id="langBtn" onclick="toggleLanguage()">EN</button>
            </div>
        </div>
    </header>

    <div class="container">
        <!-- Hero Section -->
        <section id="hero">
            <div class="hero-content">
                <div class="terminal-badge">
                    <div class="dot"></div>
                    <span>System.Ready() // .NET Core Expert</span>
                </div>
                <h1>Muhammet Akalın</h1>
                <h2 data-tr="Full Stack & .NET Yazılım Uzmanı" data-en="Full Stack & .NET Software Specialist">Full Stack & .NET Yazılım Uzmanı</h2>
                <p data-tr="Modern web teknolojileri, kurumsal mimariler ve ilişkisel veritabanı tasarımı konularında uzmanlaşmış; .NET ekosistemi ve containerization süreçlerinde yüksek performanslı çözümler üretiyorum." data-en="Specialized in modern web technologies, enterprise architectures, and relational database design; building high-performance solutions in the .NET ecosystem and containerization processes.">Modern web teknolojileri, kurumsal mimariler ve ilişkisel veritabanı tasarımı konularında uzmanlaşmış; .NET ekosistemi ve containerization süreçlerinde yüksek performanslı çözümler üretiyorum.</p>
                <div class="btn-group">
                    <a href="#projects" class="btn btn-primary"><i class="fa-solid fa-terminal"></i> <span data-tr="Projelerim" data-en="My Projects">Projelerim</span></a>
                    <a href="#contact" class="btn btn-outline"><i class="fa-solid fa-paper-plane"></i> <span data-tr="İletişime Geç" data-en="Get in Touch">İletişime Geç</span></a>
                </div>
            </div>
            <div class="hero-visual">
                <div class="code-window">
                    <div class="code-header">
                        <div class="code-dot dot-red"></div>
                        <div class="code-dot dot-yellow"></div>
                        <div class="code-dot dot-green"></div>
                        <div class="code-title">DeveloperProfile.cs</div>
                    </div>
                    <div class="code-body">
                        <span class="code-keyword">public class</span> <span class="code-class">Developer</span> : <span class="code-class">IEngineer</span><br>
                        {<br>
                        &nbsp;&nbsp;&nbsp;&nbsp;<span class="code-keyword">public string</span> Name => <span class="code-string">"Muhammet Akalın"</span>;<br>
                        &nbsp;&nbsp;&nbsp;&nbsp;<span class="code-keyword">public string[]</span> Stack => <span class="code-keyword">new</span>[] { <br>
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="code-string">"C#"</span>, <span class="code-string">"ASP.NET Core"</span>, <br>
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="code-string">"React"</span>, <span class="code-string">"Docker"</span>, <span class="code-string">"SQL"</span> <br>
                        &nbsp;&nbsp;&nbsp;&nbsp;};<br>
                        &nbsp;&nbsp;&nbsp;&nbsp;<span class="code-keyword">public bool</span> CleanArchitecture => <span class="code-keyword">true</span>;<br>
                        }
                    </div>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section id="about">
            <h3 class="section-title"><span>01.</span> <span data-tr="Hakkımda" data-en="About Me">Hakkımda</span></h3>
            <div class="about-card">
                <p data-tr="Modern web teknolojileri, kurumsal mimariler ve ilişkisel veritabanı tasarımı konularında uzmanlaşmış; .NET ekosistemi (C#, ASP.NET Core, Entity Framework Core) ve containerization (Docker) süreçlerinde yetkin Full Stack Developer [cite: Muhammet_Akalin_ozgecmis.pdf]. Otel rezervasyon sistemleri, e-ticaret platformları ve ödeme servisleri dahil olmak üzere ölçeklenebilir GitHub projeleri geliştirdim." data-en="Specialized in modern web technologies, enterprise architectures, and relational database design; a proficient Full Stack Developer in the .NET ecosystem (C#, ASP.NET Core, Entity Framework Core) and containerization (Docker) [cite: Muhammet_Akalin_ozgecmis.pdf]. I have developed scalable GitHub projects including hotel reservation systems, e-commerce platforms, and payment services.">Modern web teknolojileri, kurumsal mimariler ve ilişkisel veritabanı tasarımı konularında uzmanlaşmış; .NET ekosistemi (C#, ASP.NET Core, Entity Framework Core) ve containerization (Docker) süreçlerinde yetkin Full Stack Developer [cite: Muhammet_Akalin_ozgecmis.pdf]. Otel rezervasyon sistemleri, e-ticaret platformları ve ödeme servisleri dahil olmak üzere ölçeklenebilir GitHub projeleri geliştirdim.</p>
                <p data-tr="Temiz mimari (Clean Architecture), Unit of Work tasarım deseni ve sürdürülebilir kod yazımı odak alanlarım olup; React, TypeScript ve DevOps süreçleriyle yetkinliklerimi sürekli genişletmekteyim [cite: Muhammet_Akalin_ozgecmis.pdf]." data-en="My focus areas include Clean Architecture, Unit of Work design pattern, and sustainable coding, while continuously expanding my competencies with React, TypeScript, and DevOps processes [cite: Muhammet_Akalin_ozgecmis.pdf].">Temiz mimari (Clean Architecture), Unit of Work tasarım deseni ve sürdürülebilir kod yazımı odak alanlarım olup; React, TypeScript ve DevOps süreçleriyle yetkinliklerimi sürekli genişletmekteyim [cite: Muhammet_Akalin_ozgecmis.pdf].</p>
            </div>
        </section>

        <!-- Projects Section -->
        <section id="projects">
            <h3 class="section-title"><span>02.</span> <span data-tr="Öne Çıkan Projeler" data-en="Featured Projects">Öne Çıkan Projeler</span></h3>
            <div class="projects-grid">
                <div class="project-card">
                    <div>
                        <h3>StayHub - Rezervasyon <i class="fa-solid fa-hotel"></i></h3>
                        <p data-tr="Docker entegrasyonlu, otel ve mülk yönetim süreçlerini yöneten kapsamlı web tabanlı uygulama." data-en="Comprehensive web-based application managing hotel and property management processes with Docker integration.">Docker entegrasyonlu, otel ve mülk yönetim süreçlerini yöneten kapsamlı web tabanlı uygulama.</p>
                        <div class="tech-tags">
                            <span class="tech-tag">.NET Core</span>
                            <span class="tech-tag">SQL Server</span>
                            <span class="tech-tag">Docker</span>
                        </div>
                    </div>
                    <div class="project-links">
                        <a href="#" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square"></i> Demo</a>
                        <a href="https://github.com/muhammetakln" target="_blank"><i class="fa-brands fa-github"></i> GitHub</a>
                    </div>
                </div>

                <div class="project-card">
                    <div>
                        <h3>LibraNet - Makale Platformu <i class="fa-solid fa-book-open"></i></h3>
                        <p data-tr="Kullanıcı yetkilendirme, modern arayüz ve güvenli arka plan altyapısına sahip makale ve içerik paylaşım ağı." data-en="Article and content sharing network with user authorization, modern interface, and secure backend infrastructure.">Kullanıcı yetkilendirme, modern arayüz ve güvenli arka plan altyapısına sahip makale ve içerik paylaşım ağı.</p>
                        <div class="tech-tags">
                            <span class="tech-tag">React</span>
                            <span class="tech-tag">ASP.NET Core</span>
                            <span class="tech-tag">Identity</span>
                        </div>
                    </div>
                    <div class="project-links">
                        <a href="#" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square"></i> Demo</a>
                        <a href="https://github.com/muhammetakln" target="_blank"><i class="fa-brands fa-github"></i> GitHub</a>
                    </div>
                </div>

                <div class="project-card">
                    <div>
                        <h3 data-tr="E-Ticaret Altyapısı" data-en="E-Commerce Infrastructure">E-Ticaret Altyapısı <i class="fa-solid fa-cart-shopping"></i></h3>
                        <p data-tr="Sepet yönetimi, veri saklama ve performans optimizasyonları içeren kurumsal e-commerce projesi." data-en="Enterprise e-commerce project including cart management, data storage, and performance optimizations.">Sepet yönetimi, veri saklama ve performans optimizasyonları içeren kurumsal e-commerce projesi.</p>
                        <div class="tech-tags">
                            <span class="tech-tag">C#</span>
                            <span class="tech-tag">Entity Framework</span>
                            <span class="tech-tag">SQL</span>
                        </div>
                    </div>
                    <div class="project-links">
                        <a href="#" target="_blank"><i class="fa-solid fa-arrow-up-right-from-square"></i> Demo</a>
                        <a href="https://github.com/muhammetakln" target="_blank"><i class="fa-brands fa-github"></i> GitHub</a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section id="skills">
            <h3 class="section-title"><span>03.</span> <span data-tr="Yetenekler & Teknolojiler" data-en="Skills & Technologies">Yetenekler & Teknolojiler</span></h3>
            <div class="skills-container">
                <div class="skill-category">
                    <h4 data-tr="// Arka Plan (Backend)" data-en="// Backend"><i class="fa-solid fa-server"></i> <span data-tr="Arka Plan (Backend)" data-en="Backend">Arka Plan (Backend)</span></h4>
                    <ul class="skill-list">
                        <li><i class="fa-solid fa-check"></i> C# / .NET Core</li>
                        <li><i class="fa-solid fa-check"></i> RESTful API</li>
                        <li><i class="fa-solid fa-check"></i> Entity Framework Core</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h4 data-tr="// Veritabanı & Araçlar" data-en="// Database & Tools"><i class="fa-solid fa-database"></i> <span data-tr="Veritabanı & Araçlar" data-en="Database & Tools">Veritabanı & Araçlar</span></h4>
                    <ul class="skill-list">
                        <li><i class="fa-solid fa-check"></i> MS SQL Server / SQLite</li>
                        <li><i class="fa-solid fa-check"></i> Docker</li>
                        <li><i class="fa-solid fa-check"></i> Git / GitHub</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h4 data-tr="// Arayüz (Frontend)" data-en="// Frontend"><i class="fa-solid fa-laptop-code"></i> <span data-tr="Arayüz (Frontend)" data-en="Frontend">Arayüz (Frontend)</span></h4>
                    <ul class="skill-list">
                        <li><i class="fa-solid fa-check"></i> React.js</li>
                        <li><i class="fa-solid fa-check"></i> HTML5 / CSS3</li>
                        <li><i class="fa-solid fa-check"></i> JavaScript / TypeScript</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <h3 class="section-title"><span>04.</span> <span data-tr="İletişim" data-en="Contact">İletişim</span></h3>
            <div class="contact-grid">
                <div class="contact-item">
                    <div class="contact-icon"><i class="fa-solid fa-envelope"></i></div>
                    <div class="contact-info">
                        <span>E-posta</span>
                        <a href="mailto:akalinmuhammmetyz@gmail.com">akalinmuhammmetyz@gmail.com</a>
                    </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon"><i class="fa-solid fa-phone"></i></div>
                    <div class="contact-info">
                        <span>Telefon</span>
                        <a href="tel:05464312274">0546 431 22 74</a>
                    </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon"><i class="fa-brands fa-github"></i></div>
                    <div class="contact-info">
                        <span>GitHub</span>
                        <a href="https://github.com/muhammetakln" target="_blank">github.com/muhammetakln</a>
                    </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon"><i class="fa-brands fa-linkedin"></i></div>
                    <div class="contact-info">
                        <span>LinkedIn</span>
                        <a href="https://www.linkedin.com/in/muhammet-akal%C4%B1nn-703aa4406/" target="_blank">linkedin.com/in/muhammet-akalınn</a>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2026 Muhammet Akalın. All rights reserved. // Coded with Passion.</p>
    </footer>

    <script>
        let currentLang = 'tr';

        function toggleLanguage() {
            currentLang = currentLang === 'tr' ? 'en' : 'tr';
            document.getElementById('langBtn').innerText = currentLang === 'tr' ? 'EN' : 'TR';
            document.getElementById('html-root').setAttribute('lang', currentLang);

            const elements = document.querySelectorAll('[data-tr]');
            elements.forEach(el => {
                if (currentLang === 'en') {
                    el.innerHTML = el.getAttribute('data-en');
                } else {
                    el.innerHTML = el.getAttribute('data-tr');
                }
            });
        }
    </script>
</body>
</html>
