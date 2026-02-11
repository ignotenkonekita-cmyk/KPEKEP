<!DOCTYPE html>
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: #8a2be2;
            border-radius: 50%;
            animation: float 15s infinite linear;
            opacity: 0.3;
        }
        
        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 0.3;
            }
            90% {
                opacity: 0.3;
            }
            100% {
                transform: translateY(-10px) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* Навигация */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #8a2be2;
            padding: 1rem 0;
            z-index: 100;
        }
        
        nav .container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #8a2be2;
            text-shadow: 0 0 10px #8a2be2;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        .nav-links a {
            color: #e0e0e0;
            text-decoration: none;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 4px;
        }
        
        .nav-links a:hover {
            color: #8a2be2;
            background: rgba(138, 43, 226, 0.1);
            box-shadow: 0 0 20px rgba(138, 43, 226, 0.3);
        }
        
        /* Основной контент */
        main {
            position: relative;
            z-index: 10;
            padding-top: 80px;
        }
        
        .section {
            min-height: 100vh;
            padding: 4rem 2rem;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .container {
            max-width: 1200px;
            width: 100%;
            margin: 0 auto;
        }
        
        /* Главная секция */
        .hero {
            text-align: center;
            background: radial-gradient(circle at center, rgba(138, 43, 226, 0.1) 0%, transparent 70%);
        }
        
        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #ffffff, #8a2be2, #ffffff);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: glow 2s ease-in-out infinite alternate;
        }
        
        @keyframes glow {
            from { filter: drop-shadow(0 0 20px #8a2be2); }
            to { filter: drop-shadow(0 0 30px #8a2be2); }
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.8;
        }
        
        .server-status {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: rgba(0, 0, 0, 0.5);
            padding: 1rem 2rem;
            border-radius: 8px;
            border: 1px solid #8a2be2;
            margin-bottom: 2rem;
        }
        
        .status-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #00ff00;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(0, 255, 0, 0.7); }
            70% { box-shadow: 0 0 0 10px rgba(0, 255, 0, 0); }
            100% { box-shadow: 0 0 0 0 rgba(0, 255, 0, 0); }
        }
        
        /* Секции контента */
        .content-section {
            background: rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(138, 43, 226, 0.3);
            border-radius: 12px;
            padding: 3rem;
            margin: 2rem 0;
            backdrop-filter: blur(10px);
        }
        
        .content-section h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: #8a2be2;
            text-align: center;
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .info-card {
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(138, 43, 226, 0.5);
            border-radius: 8px;
            padding: 2rem;
            transition: all 0.3s ease;
        }
        
        .info-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(138, 43, 226, 0.3);
            border-color: #8a2be2;
        }
        
        .info-card h3 {
            color: #ffffff;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }
        
        .info-card p {
            opacity: 0.8;
            line-height: 1.6;
        }
        
        /* Правила */
        .rules-list {
            list-style: none;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .rules-list li {
            background: rgba(0, 0, 0, 0.5);
            border-left: 4px solid #8a2be2;
            padding: 1rem 1.5rem;
            margin-bottom: 1rem;
            border-radius: 0 8px 8px 0;
            transition: all 0.3s ease;
        }
        
        .rules-list li:hover {
            background: rgba(138, 43, 226, 0.1);
            transform: translateX(5px);
        }
        
        .rules-list li::before {
            content: "▸ ";
            color: #8a2be2;
            font-weight: bold;
        }
        
        /* Форма заявки */
        .application-form {
            max-width: 600px;
            margin: 0 auto;
            background: rgba(0, 0, 0, 0.5);
            padding: 2rem;
            border-radius: 12px;
            border: 1px solid rgba(138, 43, 226, 0.5);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #8a2be2;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.75rem;
            background: rgba(0, 0, 0, 0.7);
            border: 1px solid rgba(138, 43, 226, 0.5);
            border-radius: 6px;
            color: #ffffff;
            font-family: inherit;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #8a2be2;
            box-shadow: 0 0 10px rgba(138, 43, 226, 0.3);
        }
        
        .submit-btn {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(45deg, #8a2be2, #4b0082);
            border: none;
            border-radius: 8px;
            color: #ffffff;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(138, 43, 226, 0.4);
        }
        
        /* Контакты */
        .contacts {
            text-align: center;
        }
        
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .contact-link {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            padding: 1rem 2rem;
            background: rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(138, 43, 226, 0.5);
            border-radius: 8px;
            color: #ffffff;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .contact-link:hover {
            background: rgba(138, 43, 226, 0.2);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.3);
        }
        
        /* Футер */
        footer {
            text-align: center;
            padding: 2rem;
            border-top: 1px solid rgba(138, 43, 226, 0.3);
            opacity: 0.7;
        }
        
        /* Адаптивность */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .nav-links { display: none; }
            .contact-links { flex-direction: column; }
            .info-grid { grid-template-columns: 1fr; }
        }
        
        /* Скролл */
        html {
            scroll-behavior: smooth;
        }
        
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #0a0a0a;
        }
        
        ::-webkit-scrollbar-thumb {
            background: #8a2be2;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <!-- Анимированные частицы -->
    <div class="particles" id="particles"></div>
    
    <!-- Навигация -->
    <nav>
        <div class="container">
            <div class="logo">KRAKEN</div>
            <ul class="nav-links">
               <li><a href="#home">Главная</a></li>
                <li><a href="#about">О кфг</a></li>
                <li><a href="#rules">о софте</a></li>
                <li><a href="#apply"></a></li>
                <li><a href="#contacts">Контакты</a></li>
            </ul>
        </div>
    </nav>
    
    <main>
        
                        <a href="https://t.me/kpekepy" class="contact-link">
                            <span>💬</span>
                            <span>ТЕЛЕГЛАМ канал</span>
                        </a>
                        <a href="https://t.me/lost_boo_ks" class="contact-link">
                            <span>👑</span>
                            <span>Админ</span>
                        </a
        <!-- Главная секция -->
        <section id="home" class="section hero">
            
            <div class="container">
                <h1>KRAKEN</h1>
                <p>тут всё о кфг </p>
                
                <div class="server-status">
                    <div class="status-dot"></div>
                    <span>ты  онлайн</span>
                </div>
                
                <p>Добро пожаловать в мир модекаций пабга</p>
            </div>
        </section>
        
        <!-- О кфг -->
        <section id="about" class="section">
            <div class="container">
                <div class="content-section">
                    <h2>о кфг </h2>
                    <div class="info-grid">
                        <div class="info-card">
                            <h3>😉описание</h3>
                            <p>кфг это токой же фаил игры только уже отредактированы - изменяется код игры  (скин, эмоция, графика-фпс)  
                         .</p>
                        </div>
                        <div class="info-card">
                            <h3>🤔подробнее</h3>
                            <p>берётся Фаил пабга. расшифровывается код  меняется код с дорогова  скина вписывается к дешоваму скину файл сохранился и уже заменяется как обычный кфг.
                        </div>
                        <div class="info-card">
                            <h3>👥 о бене</h3>
                            <p>большинство кфг не банят но есть исключения за кфг можно получить бан. в основном банят на глобал 64 бит
                            </p>
                        </div>
                        <div class="info-card">
                            <h3>👥 о видимости кфг</h3>
                            <p>кфг виден только тебе! и у кого тоже он скачан так как только у тебя файл заменён 
                            но если отмечать то будет писать это скин какой-то ты видишь<p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Правила -->
        <section id="rules" class="section">
            <div class="container">
                <div class="content-section">
                    <h2>о софте</h2>
                    
                    <h3 style="color: #8a2be2; margin-bottom: 1rem; font-size: 1.5rem;">как не получить бан</h3>
                    <ul class="rules-list">
                        <li>не играть с аим ботом 
                        <li>не водить прицелом по модельке противника 
                        
                        <li>Ориентироваться но шаги звуки метки
                        <li>не делать больше 5-6 килов за катку </pi>
                        <li>не делать больше кд на новых аккаунтов</li>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Контакты -->
        <section id="contacts" class="section contacts">
            <div class="container">
                <div class="content-section">
                    <h2>СВЯСЬ</h2>
                    <p>привет тут</p>
                    
                    <div class="..">
                        <a href="https://t.me/kpekepy" class="contact-link">
                            <span>💬</span>
                            <span>скачать софт</span>
                        </a>
                      
                        </a>
                    </div>
                </div>
            </div>
        </section>
    </main>
    
    <footer>
        <p>&copy; 2026 KRAKEN Создано с любовью к пабгу).</p>
    </footer>
    
    <script>
        // Создание анимированных частиц
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 15 + 's';
                particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
                particlesContainer.appendChild(particle);
            }
        }
        
        // Обработка формы заявки (удалено, так как теперь используется Discord)
        
        // Плавная прокрутка для навигации
        document.querySelectorAll('nav a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
        
        // Инициализация
        document.addEventListener('DOMContentLoaded', function() {
            createParticles();
        });
        
        //
    </script>
</body>
</html>
