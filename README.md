<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TowkaVisuals · фиолет неон</title>
    <!-- Inter + Minecraft vibes -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #0b0b17;
            background-image: radial-gradient(circle at 25% 0%, #2e1a47 0%, #0c0c1a 90%);
            color: #edeaff;
            line-height: 1.5;
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* неоновые эффекты (только свечение, без слова НЕОН в тексте) */
        .neon-glow {
            text-shadow: 0 0 6px #b77eff, 0 0 12px #a35eff, 0 0 20px #8a3cff;
        }
        
        .neon-border {
            border: 2px solid #b36bff;
            box-shadow: 0 0 10px #aa5eff, inset 0 0 8px #c08aff;
        }

        /* Minecraft намёки */
        .mc-flag {
            display: inline-block;
            background: #3a2547;
            color: #ccb3ff;
            padding: 0.2rem 0.8rem;
            font-size: 0.7rem;
            letter-spacing: 0.1em;
            border: 2px solid #8b5f9e;
            image-rendering: pixelated;
            box-shadow: inset 0 0 0 2px #23162b;
            text-transform: uppercase;
        }

        .beta-tag {
            background: #5f2b8a;
            color: #f0d5ff;
            border: 2px solid #b27afe;
            box-shadow: 0 0 12px #c273ff;
            font-weight: 700;
            padding: 0.2rem 1rem;
            border-radius: 0px;
            margin-left: 1rem;
            font-size: 0.8rem;
            display: inline-block;
        }

        /* навигация */
        .navbar {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 1.5rem 0;
            border-bottom: 2px solid #5a3991;
            box-shadow: 0 4px 0 #2e1d47;
            flex-wrap: wrap;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo-icon {
            font-size: 2.4rem;
            margin-right: 0.5rem;
            color: #c285ff;
            filter: drop-shadow(0 0 8px #b45eff);
        }

        .logo-text {
            font-weight: 800;
            font-size: 2rem;
            letter-spacing: -0.02em;
            background: linear-gradient(145deg, #f0dcff, #caa6ff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 10px #bb7aff;
        }

        .nav-links a {
            margin-left: 2.5rem;
            text-decoration: none;
            color: #cfbef5;
            font-weight: 600;
            font-size: 1rem;
            transition: 0.2s;
            text-shadow: 0 0 5px #a06eff;
        }

        .nav-links a:hover {
            color: white;
            text-shadow: 0 0 10px #e2b3ff, 0 0 20px #b602ff;
        }

        /* hero */
        .hero {
            padding: 5rem 0 3rem;
            text-align: center;
        }

        .hero-marker {
            background: #2f1b44;
            border: 2px solid #a35eff;
            box-shadow: 0 0 15px #b77eff;
            padding: 0.4rem 1.6rem;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            margin-bottom: 2rem;
            color: #f0dbff;
        }

        .hero h1 {
            font-size: 4.2rem;
            font-weight: 800;
            line-height: 1.1;
            letter-spacing: -0.02em;
            max-width: 1000px;
            margin: 0 auto;
        }

        .hero .highlight {
            background: linear-gradient(145deg, #e5c3ff, #b36bff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 18px #b64aff, 0 0 40px #902dff;
        }

        .hero-sub {
            font-size: 1.3rem;
            color: #cbb5f0;
            max-width: 700px;
            margin: 1.8rem auto 2.5rem;
            text-shadow: 0 0 4px #a15aff;
        }

        .cta-buttons {
            display: flex;
            gap: 1.2rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        /* КВАДРАТНЫЕ КНОПКИ С ЗАКРУГЛЕННЫМИ КРАЯМИ (square but with rounded corners) */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.6rem;
            background: #1c102b;
            border: 2px solid #8a4fff;
            padding: 0.9rem 2.2rem;
            font-weight: 700;
            font-size: 1rem;
            color: #f2e2ff;
            text-decoration: none;
            transition: 0.2s;
            box-shadow: 0 0 15px #ac6eff, 0 4px 0 #421d6b;
            /* квадратная форма с закруглением */
            border-radius: 12px;
            /* убираем лишние скругления, но оставляем умеренные */
            cursor: pointer;
        }

        .btn-primary {
            background: #5f2b9c;
            border-color: #cb9aff;
            box-shadow: 0 0 25px #c967ff, 0 5px 0 #32134b;
        }

        .btn i {
            color: #eacaff;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 0 30px #e6a6ff, 0 7px 0 #4d1f73;
            background: #773dbb;
        }

        /* товарная сетка */
        .pricing-section {
            margin: 5rem 0;
        }

        .section-title {
            font-size: 2.8rem;
            font-weight: 800;
            letter-spacing: -0.02em;
            margin-bottom: 1rem;
            text-align: center;
            text-shadow: 0 0 10px #bb77ff, 0 0 20px #b245ff;
            /* убрали слово НЕОН из заголовков */
        }

        .section-desc {
            color: #c7aff0;
            font-size: 1.2rem;
            text-align: center;
            margin-bottom: 3.5rem;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .product-card {
            background: #151025;
            border: 3px solid #a25aff;
            box-shadow: 0 0 30px #b05eff, inset 0 0 15px #2f174b;
            padding: 2rem 1.5rem;
            display: flex;
            flex-direction: column;
            transition: 0.2s;
            position: relative;
            /* квадратные карточки с небольшим скруглением */
            border-radius: 16px;
        }

        .product-card:hover {
            border-color: #f0adff;
            box-shadow: 0 0 45px #d48aff, inset 0 0 20px #a749ff;
            transform: scale(1.02);
        }

        /* пиксельные уголки (майнкрафт деталь) */
        .product-card::before {
            content: '';
            position: absolute;
            top: -6px;
            left: -6px;
            width: 20px;
            height: 20px;
            border-top: 5px solid #b56eff;
            border-left: 5px solid #b56eff;
            filter: drop-shadow(0 0 8px magenta);
            border-radius: 4px 0 0 0;
        }

        .product-card::after {
            content: '';
            position: absolute;
            bottom: -6px;
            right: -6px;
            width: 20px;
            height: 20px;
            border-bottom: 5px solid #b56eff;
            border-right: 5px solid #b56eff;
            filter: drop-shadow(0 0 8px magenta);
            border-radius: 0 0 4px 0;
        }

        .product-name {
            font-size: 1.9rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            text-shadow: 0 0 12px #b779ff;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .product-name i {
            color: #cb9aff;
            font-size: 2rem;
        }

        .product-desc {
            color: #bdabdf;
            font-size: 0.95rem;
            margin: 0.7rem 0 1.5rem;
            flex: 1;
        }

        .price {
            font-size: 3.2rem;
            font-weight: 800;
            color: #f2dbff;
            text-shadow: 0 0 15px #c67aff, 0 0 30px #ad40ff;
            margin: 0.5rem 0;
            line-height: 1;
        }

        .price small {
            font-size: 1.2rem;
            font-weight: 400;
            color: #bba1e6;
        }

        .btn-block {
            width: 100%;
            justify-content: center;
            margin-top: 1rem;
            background: #2d1949;
            border-width: 3px;
        }

        .minecraft-badge {
            background: #382753;
            border: 3px solid #b77eff;
            color: #e9d2ff;
            padding: 0.5rem 1rem;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            margin: 2rem 0;
            box-shadow: 0 0 20px #c373ff;
            border-radius: 12px;
        }

        .footer {
            border-top: 4px solid #643aa3;
            padding: 2.5rem 0;
            margin-top: 5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            color: #b29ad9;
            text-shadow: 0 0 5px #9e5eff;
            box-shadow: 0 -8px 0 #2d1a44;
        }

        .social-links a {
            color: #ccadff;
            margin-left: 1.8rem;
            font-size: 1.5rem;
            filter: drop-shadow(0 0 8px #bf7aff);
        }

        .social-links a:hover {
            color: white;
            text-shadow: 0 0 20px #f2daff;
        }

        .fixed-brand {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #241735;
            border: 3px solid #b76eff;
            padding: 0.6rem 1.4rem;
            font-weight: 700;
            box-shadow: 0 0 25px #cc7eff;
            backdrop-filter: blur(6px);
            color: #f0dcff;
            z-index: 999;
            border-radius: 12px;
        }

        .minecraft-box {
            background: #1e1333;
            border: 4px solid #9f64d9;
            box-shadow: inset 0 0 0 4px #4b2b6b, 0 0 30px #b561ff;
            padding: 1rem;
            border-radius: 16px;
        }

        hr {
            border: 2px solid #572f8f;
            box-shadow: 0 0 12px #a853ff;
        }

        /* форма */
        input, button {
            font-family: 'Inter', sans-serif;
        }

        .email-form {
            display: flex;
            gap: 0.5rem;
            background: #1b112b;
            border: 3px solid #a162e0;
            padding: 0.5rem;
            border-radius: 12px;
        }

        .email-input {
            flex: 1;
            background: #0d0823;
            border: 2px solid #b266ff;
            padding: 1rem;
            color: white;
            border-radius: 8px;
        }
    </style>
</head>
<body>
    <div class="container">
        <nav class="navbar">
            <div class="logo">
                <i class="fas fa-cube logo-icon"></i>
                <span class="logo-text">TowkaVisuals</span>
                <span class="beta-tag">BETA</span>
            </div>
            <div class="nav-links">
                <a href="#pricing">товары</a>
                <a href="#">галерея</a>
                <a href="#">связь</a>
                <a href="#">майнкрафт</a>
            </div>
        </nav>

        <section class="hero">
            <div class="hero-marker">
                <i class="fas fa-cubes"></i> фиолет·пиксель·свечение <i class="fas fa-cube"></i>
            </div>
            <h1>
                <span class="highlight">TowkaVisuals</span> — визуальный<br>фиолетовый мир
            </h1>
            <div class="hero-sub">
                Цены 1.99$ — 19.99$, майнкрафт-эстетика и неоновое свечение
            </div>
            <div class="cta-buttons">
                <a href="#pricing" class="btn btn-primary"><i class="fas fa-cart-shopping"></i> купить</a>
                <a href="#" class="btn"><i class="fas fa-gamepad"></i> блоки</a>
            </div>
        </section>

        <!-- товарный блок -->
        <div id="pricing" class="pricing-section">
            <h2 class="section-title"><i class="fas fa-cubes"></i> ФИОЛЕТОВАЯ ГАММА <i class="fas fa-cubes"></i></h2>
            <div class="section-desc">паки / шейдеры / скины</div>

            <div class="product-grid">
                <!-- товар 1: 1.99$ -->
                <div class="product-card">
                    <div class="product-name"><i class="fas fa-cube"></i> БАЗА</div>
                    <div class="product-desc">12 текстур, обои 4K, майнкрафт-палитра</div>
                    <div class="price">1.99 <small>$</small></div>
                    <button class="btn btn-block" onclick="alert('✅ TowkaVisuals: товар «База» (1.99$) добавлен')">
                        <i class="fas fa-bolt"></i> в корзину
                    </button>
                </div>

                <!-- товар 2: 4.99$ -->
                <div class="product-card">
                    <div class="product-name"><i class="fas fa-cubes"></i> СТАНДАРТ</div>
                    <div class="product-desc">35 шейдеров + 3D-модели для Blender</div>
                    <div class="price">4.99 <small>$</small></div>
                    <button class="btn btn-block" onclick="alert('✨ TowkaVisuals: набор «Стандарт» (4.99$) добавлен')">
                        <i class="fas fa-cart-shopping"></i> в корзину
                    </button>
                </div>

                <!-- товар 3: 19.99$ -->
                <div class="product-card">
                    <div class="product-name"><i class="fas fa-dragon"></i> АЛЬТЕРНЕТ</div>
                    <div class="product-desc">Полный доступ: 200+ ресурсов, эксклюзив</div>
                    <div class="price">19.99 <small>$</small></div>
                    <button class="btn btn-block" onclick="alert('💜 TowkaVisuals: куплен «Альтернет» (19.99$)')">
                        <i class="fas fa-crown"></i> купить
                    </button>
                </div>
            </div>

            <!-- майнкрафт-акцент -->
            <div class="minecraft-badge">
                <i class="fas fa-cube" style="font-size: 1.8rem;"></i>
                <span>  зелье фиолета • все цены тестовые (бета) </span>
                <i class="fas fa-cube" style="font-size: 1.8rem;"></i>
            </div>
        </div>

        <!-- дополнительный блок -->
        <div class="minecraft-box" style="padding: 2rem; margin: 4rem 0; display: flex; flex-wrap: wrap; gap: 2rem; align-items: center; justify-content: space-between;">
            <div style="display: flex; gap: 1rem; align-items: center;">
                <i class="fas fa-crown" style="font-size: 3rem; color: #d9aeff; filter: drop-shadow(0 0 20px violet);"></i>
                <div>
                    <h3 style="font-size: 2rem; font-weight: 800; text-shadow: 0 0 10px #c373ff;">VIP набор</h3>
                    <p style="color: #cfb5fc;">эксклюзивный доступ</p>
                </div>
            </div>
            <button class="btn btn-primary" onclick="alert('⚡ VIP доступ (бета)')">
                <i class="fas fa-cube"></i> 9.99$ demo
            </button>
        </div>

        <!-- форма -->
        <div style="text-align: center; margin: 5rem 0 2rem;">
            <h2 class="section-title" style="font-size: 2.2rem;">получить код</h2>
            <div class="email-form" style="max-width: 600px; margin: 0 auto;">
                <input type="email" placeholder="ваш email" id="neon-email" class="email-input">
                <button class="btn btn-primary" style="margin:0;" onclick="let v=document.getElementById('neon-email').value; if(v) alert('код отправлен на ' + v); else alert('✧ введи email')">
                    <i class="fas fa-paper-plane"></i> выслать
                </button>
            </div>
            <div class="mc-flag" style="margin-top: 1.5rem;">только для настоящих крафтеров</div>
        </div>

        <hr>

        <footer class="footer">
            <div><i class="fas fa-cube"></i> TowkaVisuals beta · вместо PulseVisuals.pro</div>
            <div>© 2025 фиолетовая версия</div>
            <div class="social-links">
                <a href="#"><i class="fab fa-discord"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-twitch"></i></a>
            </div>
        </footer>
    </div>

    <!-- фиксированная плашка -->
    <div class="fixed-brand">
        <i class="fas fa-cube"></i> TowkaVisuals · фиолет <i class="fas fa-cube"></i>
    </div>
</body>
</html>
