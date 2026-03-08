<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мамочке ❤️ С 8 марта!</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #fadadd;
            background-image: radial-gradient(circle at 30% 40%, #ffdbdb 0%, transparent 30%),
                              radial-gradient(circle at 80% 70%, #ffc1cc 0%, transparent 40%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            font-family: 'Georgia', 'Times New Roman', serif;
            padding: 15px;
        }

        /* Конверт-открытка */
        .envelope {
            max-width: 750px;
            width: 100%;
            background: #fff9fa;
            border-radius: 40px 40px 120px 120px;
            padding: 30px 30px 60px;
            box-shadow: 0 30px 40px rgba(199, 90, 120, 0.3),
                        0 0 0 12px #ffe4e9,
                        0 0 0 18px #ffb6c9;
            position: relative;
            border: 3px solid white;
        }

        /* Сердечко-застёжка */
        .heart-closure {
            position: absolute;
            top: -25px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 60px;
            filter: drop-shadow(0 8px 5px #ff90aa);
            animation: heartbeat 1.5s infinite;
            z-index: 5;
        }

        @keyframes heartbeat {
            0% { transform: translateX(-50%) scale(1); }
            30% { transform: translateX(-50%) scale(1.2); }
            50% { transform: translateX(-50%) scale(1); }
            70% { transform: translateX(-50%) scale(1.1); }
            100% { transform: translateX(-50%) scale(1); }
        }

        /* Главный заголовок */
        .main-title {
            text-align: center;
            margin: 30px 0 25px;
            position: relative;
        }

        h1 {
            font-size: 4.5em;
            color: #c93e6b;
            text-shadow: 3px 3px 0 #ffd9e2, 5px 5px 0 #ffb0c3;
            line-height: 1.2;
            margin-bottom: 10px;
            font-family: 'Brush Script MT', cursive;
            transform: rotate(-1deg);
        }

        .main-title p {
            font-size: 2em;
            color: #a53f60;
            background: #fff0f3;
            display: inline-block;
            padding: 10px 35px;
            border-radius: 40px;
            border: 3px dotted #ff90b0;
            font-style: italic;
        }

        /* Фото рамка (для мамы) */
        .photo-frame {
            width: 250px;
            height: 250px;
            margin: 20px auto;
            border-radius: 50%;
            background: #ffe7ed;
            border: 10px solid white;
            box-shadow: 0 10px 0 #ffb0c3, 0 20px 25px rgba(200, 80, 110, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            position: relative;
        }

        .photo-frame::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, transparent 60%, rgba(255, 200, 220, 0.4));
        }

        .photo-content {
            font-size: 150px;
            line-height: 1;
            transform: scaleX(-1);
            filter: drop-shadow(5px 5px 5px rgba(0,0,0,0.1));
        }

        /* Блок с обращением */
        .letter {
            background: #fff5f8;
            border-radius: 80px 30px 80px 30px;
            padding: 35px;
            margin: 30px 0;
            border: 5px dashed #ff96b5;
            position: relative;
        }

        .letter::before {
            content: "💗";
            position: absolute;
            top: -25px;
            left: 40px;
            font-size: 45px;
            background: white;
            padding: 5px 20px;
            border-radius: 50px;
            border: 3px solid #ff96b5;
            transform: rotate(-15deg);
        }

        .greeting {
            font-size: 2em;
            color: #9d3e5b;
            margin-bottom: 20px;
            font-weight: bold;
            text-align: center;
        }

        .letter-text {
            font-size: 1.4em;
            color: #543847;
            line-height: 1.8;
            text-align: center;
            margin-bottom: 20px;
        }

        .letter-text i {
            color: #d44e78;
            font-size: 1.2em;
        }

        .signature {
            text-align: right;
            font-size: 1.8em;
            color: #b34169;
            font-family: 'Brush Script MT', cursive;
            border-top: 3px wavy #ffa5bc;
            padding-top: 20px;
            margin-top: 20px;
        }

        /* Список "За что я люблю маму" */
        .why-i-love {
            background: #ffeef2;
            border-radius: 60px;
            padding: 30px;
            margin: 30px 0;
            border: 5px solid white;
            box-shadow: inset 0 0 0 4px #ffb7cc;
        }

        .why-i-love h2 {
            font-size: 2.5em;
            color: #ba3f66;
            text-align: center;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
        }

        .reasons {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .reason {
            background: white;
            padding: 15px 30px;
            border-radius: 50px;
            font-size: 1.3em;
            color: #663344;
            border: 4px solid;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .reason:hover {
            transform: translateX(10px);
            background: #fff9fb;
        }

        .reason:nth-child(1) { border-color: #ffb0c0; }
        .reason:nth-child(2) { border-color: #c5a1ff; }
        .reason:nth-child(3) { border-color: #a7e0ff; }
        .reason:nth-child(4) { border-color: #ffd5a7; }
        .reason:nth-child(5) { border-color: #c4e6a3; }

        .reason-marker {
            font-size: 2em;
        }

        /* Календарик-напоминалка */
        .date-box {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 25px 0;
        }

        .date-circle {
            width: 90px;
            height: 90px;
            background: #ffa5bc;
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            box-shadow: 0 10px 0 #ac4d6e;
            border: 4px solid #ffe2ec;
        }

        .date-circle .big {
            font-size: 2.2em;
            line-height: 1;
        }

        .date-circle .small {
            font-size: 0.9em;
            text-transform: uppercase;
        }

        .date-text {
            font-size: 1.7em;
            color: #a53f60;
            align-self: center;
            font-style: italic;
        }

        /* Стикеры с пожеланиями для мамы */
        .wishes-row {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin: 40px 0;
        }

        .wish-sticker {
            background: #fcf0f5;
            padding: 18px 25px;
            border-radius: 40px 10px 40px 10px;
            font-size: 1.2em;
            border: 4px solid white;
            box-shadow: 0 7px 0 #ffb0c3;
            transform: rotate(var(--r));
            flex: 1 1 150px;
            text-align: center;
            color: #722b48;
            font-weight: bold;
        }

        .wish-sticker:nth-child(1) { --r: -2deg; background: #ffe1f0; }
        .wish-sticker:nth-child(2) { --r: 3deg; background: #ffe7d4; }
        .wish-sticker:nth-child(3) { --r: -1deg; background: #e2f0ff; }
        .wish-sticker:nth-child(4) { --r: 2deg; background: #e6ffe6; }
        .wish-sticker:nth-child(5) { --r: -3deg; background: #ffe0f5; }
        .wish-sticker:nth-child(6) { --r: 1deg; background: #fff3d3; }

        .wish-sticker:hover {
            transform: scale(1.05) rotate(0deg);
            z-index: 5;
        }

        /* Кнопка "Сюрприз для мамы" */
        .surprise-section {
            text-align: center;
            margin: 40px 0 20px;
        }

        .mom-btn {
            background: #ff749c;
            color: white;
            border: none;
            font-size: 2.8em;
            font-family: 'Georgia', serif;
            padding: 25px 50px;
            border-radius: 120px;
            cursor: pointer;
            box-shadow: 0 15px 0 #b14064;
            border: 5px solid #ffb7d0;
            transition: 0.05s linear;
            font-weight: bold;
            letter-spacing: 2px;
            position: relative;
        }

        .mom-btn:active {
            transform: translateY(8px);
            box-shadow: 0 7px 0 #b14064;
        }

        .surprise-display {
            background: #ffe3f0;
            padding: 40px;
            border-radius: 90px;
            font-size: 2.2em;
            margin-top: 35px;
            border: 8px double #ff80a5;
            display: none;
            animation: magic 0.8s;
            color: #712d49;
            line-height: 1.6;
        }

        .surprise-display.show {
            display: block;
        }

        @keyframes magic {
            0% { opacity: 0; transform: scale(0.1) rotate(-10deg); }
            70% { transform: scale(1.1) rotate(3deg); }
            100% { opacity: 1; transform: scale(1) rotate(0); }
        }

        /* Нижний колонтитул */
        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 4px dotted #ffb0c3;
        }

        .footer p {
            font-size: 1.5em;
            color: #a53f60;
        }

        .footer-flowers {
            font-size: 2.5em;
            margin-top: 15px;
            animation: sway 3s infinite;
        }

        @keyframes sway {
            0% { letter-spacing: 5px; }
            50% { letter-spacing: 15px; }
            100% { letter-spacing: 5px; }
        }

        /* Адаптация */
        @media (max-width: 600px) {
            h1 {
                font-size: 3.2em;
            }
            
            .photo-frame {
                width: 180px;
                height: 180px;
            }
            
            .photo-content {
                font-size: 100px;
            }
            
            .greeting {
                font-size: 1.6em;
            }
            
            .letter-text {
                font-size: 1.1em;
            }
            
            .mom-btn {
                font-size: 2em;
                padding: 20px 30px;
            }
            
            .reason {
                font-size: 1.1em;
            }
            
            .date-circle {
                width: 70px;
                height: 70px;
            }
            
            .date-text {
                font-size: 1.3em;
            }
        }
    </style>
</head>
<body>
    <div class="envelope">
        <!-- Сердечко сверху -->
        <div class="heart-closure">❤️</div>

        <!-- Заголовок -->
        <div class="main-title">
            <h1>Мамочке</h1>
            <p>С 8 марта!</p>
        </div>

        <!-- Фоторамка (символ мамы) -->
        <div class="photo-frame">
            <div class="photo-content">👩🏻</div>
        </div>

        <!-- Письмо маме -->
        <div class="letter">
            <div class="greeting">💗 Мамочка, родная! 💗</div>
            <div class="letter-text">
                <i>Самой красивой, самой нежной,</i><br>
                <i>Самой любимой и родной!</i><br><br>
                Поздравляю тебя с 8 марта!<br>
                Спасибо тебе за всё: за тепло, заботу,<br>
                за ласку и поддержку. Ты — мой ангел-хранитель.<br>
                <b>Желаю тебе здоровья, счастья и весеннего настроения!</b>
            </div>
            <div class="signature">
                Твой сын        ❤️ 
            </div>
        </div>

        <!-- "За что я люблю маму" -->
        <div class="why-i-love">
            <h2>
                <span>✨</span>
                За что я тебя
                <span>✨</span>
            </h2>
            <div class="reasons">
                <div class="reason">
                    <span class="reason-marker">💕</span>
                    За твои тёплые объятия
                </div>
                <div class="reason">
                    <span class="reason-marker">🥘</span>
                    За самую вкусную еду
                </div>
                <div class="reason">
                    <span class="reason-marker">😊</span>
                    За твою улыбку
                </div>
                <div class="reason">
                    <span class="reason-marker">🤗</span>
                    За то, что всегда поддерживаешь
                </div>
                <div class="reason">
                    <span class="reason-marker">🌟</span>
                    За то, что ты просто есть
                </div>
            </div>
        </div>

        <!-- Календарь (дата) -->
        <div class="date-box">
            <div class="date-circle">
                <span class="big">8</span>
                <span class="small">марта</span>
            </div>
            <div class="date-text">Твой день</div>
            <div class="date-circle">
                <span class="big">❤️</span>
                <span class="small">2026</span>
            </div>
        </div>

        <!-- Пожелания для мамы стикерами -->
        <div class="wishes-row">
            <div class="wish-sticker">🌸 Весеннего настроения</div>
            <div class="wish-sticker">💐 Море цветов</div>
            <div class="wish-sticker">😊 Радости каждый день</div>
            <div class="wish-sticker">💖 Крепкого здоровья</div>
            <div class="wish-sticker">✨ Исполнения желаний</div>
            <div class="wish-sticker">☀️ Тепла и света</div>
        </div>

        <!-- Сюрприз для мамы -->
        <div class="surprise-section">
            <button class="mom-btn" onclick="showMomSurprise()">🎁 ДЛЯ МАМЫ</button>
            <div id="momSurprise" class="surprise-display">
                ❤️❤️❤️❤️❤️❤️❤️❤️❤️<br>
                МАМОЧКА, ТЫ ЛУЧШАЯ!<br>
                ❤️❤️❤️❤️❤️❤️❤️❤️❤️
            </div>
        </div>

        <!-- Подвал -->
        <div class="footer">
            <p>С любовью и благодарностью</p>
            <div class="footer-flowers">🌸🌼🌺🌷🌹</div>
            <p style="font-size: 1.2em; margin-top: 15px;">8 марта 2026</p>
        </div>
    </div>

    <script>
        function showMomSurprise() {
            const surprise = document.getElementById('momSurprise');
            surprise.classList.toggle('show');
            
            if (surprise.classList.contains('show')) {
                // Запускаем сердечки
                for (let i = 0; i < 15; i++) {
                    setTimeout(() => {
                        const heart = document.createElement('div');
                        const hearts = ['❤️', '💗', '💖', '💘', '💝', '💕'];
                        heart.innerText = hearts[Math.floor(Math.random() * hearts.length)];
                        heart.style.position = 'fixed';
                        heart.style.left = Math.random() * 100 + '%';
                        heart.style.top = '-20px';
                        heart.style.fontSize = (25 + Math.random() * 30) + 'px';
                        heart.style.zIndex = '9999';
                        heart.style.pointerEvents = 'none';
                        heart.style.animation = `floatDown ${3 + Math.random() * 3}s linear`;
                        heart.style.filter = 'drop-shadow(0 5px 5px #ffb0c0)';
                        document.body.appendChild(heart);
                        
                        setTimeout(() => heart.remove(), 6000);
                    }, i * 120);
                }
            }
            
            // Добавляем стили анимации если ещё нет
            if (!document.getElementById('floatStyle')) {
                const style = document.createElement('style');
                style.id = 'floatStyle';
                style.textContent = `
                    @keyframes floatDown {
                        0% { transform: translateY(0) rotate(0deg); opacity: 1; }
                        100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
                    }
                `;
                document.head.appendChild(style);
            }
        }
    </script>
</body>
</html>
