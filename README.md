<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be Mine? 💕</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            padding: 20px;
        }

        .container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            padding: 40px;
            max-width: 500px;
            width: 100%;
            text-align: center;
            animation: slideIn 0.6s ease-out;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .heart {
            font-size: 60px;
            margin-bottom: 20px;
            animation: heartBeat 1.5s ease-in-out infinite;
        }

        @keyframes heartBeat {
            0%, 100% { transform: scale(1); }
            25% { transform: scale(1.1); }
            50% { transform: scale(1.2); }
        }

        h1 {
            color: #e74c3c;
            font-size: 2.5em;
            margin-bottom: 15px;
            font-weight: 700;
        }

        .subtitle {
            color: #764ba2;
            font-size: 1.1em;
            margin-bottom: 30px;
            font-style: italic;
        }

        .rose-border {
            border-top: 3px solid #e74c3c;
            border-bottom: 3px solid #e74c3c;
            padding: 20px 0;
            margin: 30px 0;
        }

        .message {
            color: #555;
            font-size: 1.1em;
            line-height: 1.6;
            margin-bottom: 30px;
        }

        .buttons-container {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        button {
            padding: 15px 40px;
            font-size: 1.1em;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .yes-btn {
            background: linear-gradient(135deg, #e74c3c, #c0392b);
            color: white;
            box-shadow: 0 5px 15px rgba(231, 76, 60, 0.4);
        }

        .yes-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(231, 76, 60, 0.6);
        }

        .yes-btn:active {
            transform: scale(0.98);
        }

        .no-btn {
            background: linear-gradient(135deg, #95a5a6, #7f8c8d);
            color: white;
            box-shadow: 0 5px 15px rgba(149, 165, 166, 0.4);
            position: relative;
        }

        .no-btn:hover {
            transform: translate(20px, -20px);
            box-shadow: 0 8px 20px rgba(149, 165, 166, 0.6);
        }

        .games-section {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 25px;
            margin-top: 30px;
        }

        .games-title {
            color: #764ba2;
            font-size: 1.3em;
            margin-bottom: 20px;
            font-weight: 600;
        }

        .game {
            margin-bottom: 20px;
        }

        .game-label {
            color: #555;
            font-size: 0.95em;
            margin-bottom: 10px;
            font-weight: 500;
        }

        .love-meter {
            width: 100%;
            height: 20px;
            background: #ddd;
            border-radius: 10px;
            overflow: hidden;
            margin: 10px 0;
        }

        .love-fill {
            height: 100%;
            background: linear-gradient(90deg, #e74c3c, #f39c12);
            width: 0%;
            transition: width 0.5s ease;
            border-radius: 10px;
        }

        .luck-wheel {
            width: 150px;
            height: 150px;
            margin: 0 auto;
            background: conic-gradient(#e74c3c 0deg 90deg, #f39c12 90deg 180deg, #e74c3c 180deg 270deg, #f39c12 270deg 360deg);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-weight: 700;
            color: white;
            font-size: 1.2em;
            transition: transform 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .luck-wheel:hover {
            transform: scale(1.05) rotate(10deg);
        }

        .luck-wheel:active {
            animation: spin 0.5s linear;
        }

        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .confetti {
            position: fixed;
            pointer-events: none;
            font-size: 2em;
        }

        .success-message {
            color: #e74c3c;
            font-size: 1.3em;
            font-weight: 700;
            margin-top: 20px;
            animation: bounce 0.6s ease;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .flower {
            display: inline-block;
            margin: 0 5px;
            animation: sway 2s ease-in-out infinite;
        }

        @keyframes sway {
            0%, 100% { transform: rotate(-5deg); }
            50% { transform: rotate(5deg); }
        }

        @media (max-width: 600px) {
            .container {
                padding: 30px 20px;
            }
            h1 {
                font-size: 2em;
            }
            .heart {
                font-size: 50px;
            }
            button {
                padding: 12px 30px;
                font-size: 0.95em;
            }
            .buttons-container {
                gap: 15px;
            }
            .message {
                font-size: 1em;
            }
        }

        html, body {
            width: 100%;
            overflow-x: hidden;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="heart">💕</div>
        <h1>Will You Be Mine?</h1>
        <p class="subtitle">A Special Question from Someone Special 💌</p>
        
        <div class="rose-border">
            <p class="message">
                You make every day special. Your smile lights up my world, and every moment with you feels like a dream. 
                <br><br>
                I can't imagine life without you. So what do you say... 
                <span class="flower">🌹</span>
            </p>
        </div>

        <div class="buttons-container">
            <button class="yes-btn" onclick="handleYes()">YES! 💕</button>
            <button class="no-btn" id="noBtn" onmouseover="moveButton()" onclick="moveButton()">No</button>
        </div>

        <div id="successMessage"></div>

        <div class="games-section">
            <p class="games-title">🎮 Play a Game: How Much Do You Love Me?</p>
            
            <div class="game">
                <p class="game-label">Click the heart to fill the love meter:</p>
                <div class="love-meter">
                    <div class="love-fill" id="loveFill"></div>
                </div>
                <button onclick="increaseLove()" style="background: #e74c3c; color: white; padding: 8px 20px; font-size: 0.9em; margin-top: 10px;">
                    ❤️ Add Love
                </button>
            </div>

            <div class="game">
                <p class="game-label">Spin the Wheel of Destiny:</p>
                <div class="luck-wheel" onclick="spinWheel()">SPIN!</div>
                <p id="wheelResult" style="margin-top: 15px; font-size: 0.95em; color: #555; min-height: 20px;"></p>
            </div>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById('noBtn');
        let noButtonClicks = 0;

        function moveButton() {
            const randomX = (Math.random() - 0.5) * 200;
            const randomY = (Math.random() - 0.5) * 150;
            
            noBtn.style.transform = `translate(${randomX}px, ${randomY}px)`;
            noButtonClicks++;

            if (noButtonClicks === 5) {
                alert("Why are you running away? 😂 Just say YES already!");
            }
            if (noButtonClicks === 10) {
                alert("I see you're having fun! But you know what... YES is the only correct answer! 😉");
            }
        }

        function handleYes() {
            document.querySelector('.container').style.animation = 'pulse 0.6s ease';
            createConfetti();
            
            const successMsg = document.getElementById('successMessage');
            successMsg.innerHTML = `
                <div class="success-message">
                    🎉 YES!!! You Made Me The Happiest! 🎉
                    <br><br>
                    I Love You So Much! 💕
                    <br>
                    <span class="flower">🌹</span>
                    <span class="flower">🌹</span>
                    <span class="flower">🌹</span>
                </div>
            `;
            
            setTimeout(() => {
                alert("You're the best decision I could ever hope for! Let's celebrate! 🥂💕");
            }, 1000);
        }

        function createConfetti() {
            const confettiPieces = ['🎉', '💕', '🌹', '✨', '💐', '🎊', '💑', '👑'];
            
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.textContent = confettiPieces[Math.floor(Math.random() * confettiPieces.length)];
                confetti.style.left = Math.random() * window.innerWidth + 'px';
                confetti.style.top = '-20px';
                confetti.style.opacity = Math.random();
                
                document.body.appendChild(confetti);
                
                const duration = 2 + Math.random() * 1;
                const xMove = (Math.random() - 0.5) * 200;
                
                confetti.animate([
                    { transform: 'translateY(0px) translateX(0px) rotate(0deg)', opacity: 1 },
                    { transform: `translateY(${window.innerHeight}px) translateX(${xMove}px) rotate(360deg)`, opacity: 0 }
                ], {
                    duration: duration * 1000,
                    easing: 'cubic-bezier(0.25, 0.46, 0.45, 0.94)'
                });
                
                setTimeout(() => confetti.remove(), duration * 1000);
            }
        }

        let loveLevel = 0;

        function increaseLove() {
            loveLevel = Math.min(loveLevel + 15, 100);
            document.getElementById('loveFill').style.width = loveLevel + '%';
            
            if (loveLevel === 100) {
                alert("OMG! The love meter is FULL! That's all the love in the world! 💕💕💕");
            }
        }

        function spinWheel() {
            const outcomes = [
                "You will DEFINITELY say Yes! 💯",
                "True Love is in your destiny! 💕",
                "The stars align for us! ✨",
                "Soulmates detected! 🎯",
                "Forever starts today! 👑",
                "My heart chose you! 💗",
                "Fate brought us together! 🌟",
                "You're my everything! 💑"
            ];
            
            const randomIndex = Math.floor(Math.random() * outcomes.length);
            document.getElementById('wheelResult').textContent = outcomes[randomIndex];
        }

        let clickCount = 0;
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Enter') {
                clickCount++;
                if (clickCount === 3) {
                    alert("Psst... I think you should click YES! 😉💕");
                    clickCount = 0;
                }
            }
        });

        const style = document.createElement('style');
        style.textContent = `
            @keyframes pulse {
                0%, 100% { transform: scale(1); }
                50% { transform: scale(1.02); }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
