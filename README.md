<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rafail Ahmadov · Tech Entrepreneur</title>
    <!-- Font & minimal reset -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #0b0c0e;  /* тёмный фон, близкий к черному */
            font-family: 'Inter', sans-serif;
            color: #ffffff;
            line-height: 1.3;
            scroll-behavior: smooth;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 32px;
        }

        /* акцентные цвета */
        .blue {
            color: #1055D7;
        }
        .red {
            color: #FA1826;
        }

        /* типографика как у стартап-фаундеров: крупная, смелая */
        h1 {
            font-size: clamp(3.5rem, 12vw, 5.5rem);
            font-weight: 700;
            letter-spacing: -0.03em;
            line-height: 1.0;
            margin-bottom: 0.25rem;
        }

        .badge-tag {
            font-size: 1.2rem;
            font-weight: 500;
            color: #a0a5b0;
            display: block;
            margin-bottom: 1rem;
            letter-spacing: -0.01em;
        }

        .hero-sub {
            font-size: clamp(1.25rem, 4vw, 1.8rem);
            font-weight: 400;
            color: #c7cad1;
            max-width: 700px;
            margin: 1.5rem 0 2.5rem;
            line-height: 1.4;
        }

        /* кнопки в стиле tech/minimal */
        .btn-group {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin: 2.5rem 0 3rem;
        }

        .btn {
            padding: 0.9rem 2.2rem;
            border-radius: 60px;
            font-weight: 600;
            font-size: 1.2rem;
            text-decoration: none;
            transition: all 0.15s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            border: 1.5px solid transparent;
        }

        .btn-primary {
            background-color: #1055D7;
            color: white;
            box-shadow: 0 8px 18px rgba(16, 85, 215, 0.25);
        }

        .btn-primary:hover {
            background-color: #0f4abc;
            transform: scale(1.02);
            box-shadow: 0 12px 24px rgba(16, 85, 215, 0.4);
        }

        .btn-outline {
            background-color: transparent;
            border-color: #2e333d;
            color: white;
        }

        .btn-outline:hover {
            border-color: #1055D7;
            background-color: rgba(16, 85, 215, 0.05);
        }

        /* секции */
        section {
            padding: 90px 0 70px;
            border-bottom: 1px solid #1f2127;
        }

        .section-title {
            font-size: 2.8rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            margin-bottom: 3rem;
            position: relative;
            display: inline-block;
        }
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -12px;
            left: 0;
            width: 90px;
            height: 6px;
            background: linear-gradient(90deg, #1055D7 0%, #FA1826 100%);
            border-radius: 4px;
        }

        /* about grid */
        .about-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 50px;
            justify-content: space-between;
        }

        .about-text {
            flex: 2;
            min-width: 300px;
        }

        .about-text p {
            font-size: 1.4rem;
            font-weight: 400;
            color: #d3d7df;
            margin-bottom: 2rem;
            line-height: 1.5;
        }

        .founder-note {
            font-size: 1.1rem;
            color: #a5aab5;
            border-left: 4px solid #FA1826;
            padding-left: 24px;
            margin-top: 30px;
        }

        .ventures {
            flex: 1;
            min-width: 240px;
            background: #13161c;
            padding: 32px;
            border-radius: 32px;
            border: 1px solid #262b34;
        }

        .venture-item {
            margin-bottom: 30px;
        }

        .venture-item h3 {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            line-height: 1.2;
        }
        .venture-item .blue {
            color: #1055D7;
        }
        .venture-item .red {
            color: #FA1826;
        }
        .venture-item p {
            color: #949aa7;
            font-size: 0.95rem;
            margin-top: 5px;
        }

        /* карточка проекта (одна, но мощная) */
        .project-card {
            background: linear-gradient(145deg, #12151c 0%, #0b0e13 100%);
            border-radius: 40px;
            padding: 48px;
            border: 1px solid #2b313c;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            transition: all 0.2s;
        }
        .project-card:hover {
            border-color: #1055D7;
            box-shadow: 0 30px 40px -20px rgba(16,85,215,0.4);
        }

        .project-info h2 {
            font-size: 3.2rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            background: linear-gradient(130deg, #ffffff 0%, #b0b7c9 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 12px;
        }

        .project-info p {
            font-size: 1.3rem;
            color: #b1b8c5;
            max-width: 500px;
        }

        .project-badge {
            background-color: #1055D7;
            border-radius: 100px;
            padding: 12px 32px;
            font-weight: 600;
            font-size: 1.2rem;
            color: white;
            border: 1px solid rgba(255,255,255,0.1);
            backdrop-filter: blur(4px);
            white-space: nowrap;
        }

        /* mission */
        .mission-block {
            background: #0f1219;
            border-radius: 50px;
            padding: 64px 48px;
            border: 1px solid #292f3a;
            text-align: center;
        }

        .mission-quote {
            font-size: 2.5rem;
            font-weight: 600;
            line-height: 1.3;
            max-width: 900px;
            margin: 0 auto;
            color: white;
            letter-spacing: -0.02em;
        }

        .mission-quote span {
            color: #1055D7;
            border-bottom: 3px solid #FA1826;
        }

        /* footer */
        .footer {
            padding: 48px 0 56px;
            border-bottom: none;
        }

        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 30px;
        }

        .footer-left .logo-name {
            font-size: 2rem;
            font-weight: 700;
            letter-spacing: -0.02em;
        }
        .footer-left .descr {
            color: #888f9e;
            font-size: 1.1rem;
            margin-top: 8px;
        }

        .footer-social {
            display: flex;
            gap: 28px;
        }

        .footer-social a {
            color: #b5bccb;
            text-decoration: none;
            font-weight: 500;
            font-size: 1.3rem;
            transition: color 0.1s;
        }

        .footer-social a:hover {
            color: #1055D7;
        }

        /* простые разделители */
        hr {
            border: none;
            height: 1px;
            background: #262b34;
            margin: 0;
        }

        /* адаптивность */
        @media (max-width: 700px) {
            .container { padding: 0 24px; }
            h1 { font-size: 3.2rem; }
            .section-title { font-size: 2.2rem; }
            .project-card { padding: 32px; flex-direction: column; align-items: flex-start; gap: 25px; }
            .project-info h2 { font-size: 2.5rem; }
            .mission-quote { font-size: 1.8rem; }
            .btn-group .btn { padding: 0.8rem 1.8rem; font-size: 1rem; }
        }
    </style>
</head>
<body>

    <!-- HERO SECTION (первый экран) -->
    <div class="container" style="padding-top: 60px; padding-bottom: 20px;">
        <!-- верхнее микро-инфо (необязательно, но добавляет воздуха) -->
        <div class="badge-tag">Rafail Ahmadov · Baku / Global</div>
        <h1>Rafail<br>Ahmadov</h1>
        <div style="font-size: 1.6rem; font-weight: 500; color: #a5aab5; margin-top: -5px;">Young Tech Entrepreneur • Founder of PracticeX</div>
        
        <div class="hero-sub">
            Building platforms that help people learn, grow and succeed in the digital world.
        </div>

        <div class="btn-group">
            <a href="#" class="btn btn-primary">🚀 Explore My Projects</a>
            <a href="#" class="btn btn-outline">📬 Contact Me</a>
        </div>

        <!-- краткий индикатор возраста / энергии (опционально) -->
        <div style="display: flex; gap: 30px; color: #6b7380; font-weight: 500; margin-top: 30px;">
            <span>⚡ 16 y.o. first platform</span>
            <span>🌍 10k+ users</span>
            <span>🎯 AI + education</span>
        </div>
    </div>

    <!-- ABOUT ME -->
    <section>
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-grid">
                <div class="about-text">
                    <p>I am a young entrepreneur, developer, and creator of educational technology platforms.<br>My mission is simple — build tools that help people unlock their potential.</p>
                    <p style="font-size: 1.25rem;">At 16, I started building platforms that combine technology, education, and entrepreneurship.</p>
                    <div class="founder-note">
                        <span style="font-weight: 700;">I believe the future belongs to those who build, not just consume.</span>
                    </div>
                </div>
                <div class="ventures">
                    <div class="venture-item">
                        <h3><span class="blue">Practice</span><span class="red">X</span></h3>
                        <p>global SAT preparation platform with tests, analytics, and learning tools.</p>
                    </div>
                    <div class="venture-item">
                        <h3><span style="color: #ffffff;">Voice</span><span class="red">X</span></h3>
                        <p>real-time AI voice translation technology</p>
                    </div>
                    <div class="venture-item">
                        <h3 style="font-size:1.6rem;">AI + EdTech</h3>
                        <p>innovation projects at the intersection of AI, education & entrepreneurship</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ПРОЕКТЫ (PracticeX выделен) -->
    <section>
        <div class="container">
            <h2 class="section-title">Flagship project</h2>
            <div class="project-card">
                <div class="project-info">
                    <h2>PracticeX</h2>
                    <p>A global SAT preparation platform with tests, analytics, and adaptive learning tools. Built for the next generation.</p>
                </div>
                <div class="project-badge">
                    ⚡ since 2024
                </div>
            </div>
            <!-- можно добавить еще одну строчку с VoiceX, но минимализм требует оставить так -->
            <div style="margin-top: 30px; display: flex; gap: 20px; flex-wrap: wrap; justify-content: flex-end;">
                <span style="color: #7b8495;">+ VoiceX (AI voice translation) </span>
                <span style="color: #7b8495;">+ R&D lab</span>
            </div>
        </div>
    </section>

    <!-- MY MISSION -->
    <section>
        <div class="container">
            <div class="mission-block">
                <div class="mission-quote">
                    To create technology that <span>empowers people</span> to learn faster, think bigger, and build the future.
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <div class="footer container">
        <div class="footer-content">
            <div class="footer-left">
                <div class="logo-name">Rafail Ahmadov</div>
                <div class="descr">Tech Entrepreneur | Founder of PracticeX</div>
            </div>
            <div class="footer-social">
                <a href="#" target="_blank">Email</a>
                <a href="#" target="_blank">LinkedIn</a>
                <a href="#" target="_blank">Instagram</a>
            </div>
        </div>
        <!-- маленькая подпись с акцентной линией -->
        <div style="margin-top: 50px; color: #3a4150; font-size: 0.9rem; border-top: 1px solid #20242c; padding-top: 25px; display: flex; justify-content: space-between;">
            <span>© 2025 Rafail Ahmadov — build with purpose</span>
            <span style="color:#1055D7;">#buildnotconsume</span>
        </div>
    </div>

    <!-- микро-анимация при наведении на "Rafail Ahmadov" (совсем лёгкая) -->
</body>
</html>
