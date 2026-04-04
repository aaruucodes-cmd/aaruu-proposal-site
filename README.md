<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To My Love Sanskriti 💕 - Will You Forgive Me?</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(-45deg, #ff9a9e, #fecfef, #fecfef, #ff6b9d);
            background-size: 400% 400%;
            animation: loveGradient 15s ease infinite;
            min-height: 100vh;
            color: #fff;
            overflow-x: hidden;
            position: relative;
        }
        
        @keyframes loveGradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .hearts-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            overflow: hidden;
        }
        
        .heart {
            position: absolute;
            font-size: clamp(1rem, 3vw, 2rem);
            animation: float 6s linear infinite;
        }
        
        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        .container {
            max-width: 500px;
            margin: 0 auto;
            padding: clamp(1rem, 5vh, 2rem);
            position: relative;
            z-index: 10;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .card {
            background: rgba(255,255,255,0.15);
            backdrop-filter: blur(20px);
            border-radius: 25px;
            padding: clamp(1.5rem, 4vh, 3rem);
            margin-bottom: 2rem;
            border: 1px solid rgba(255,255,255,0.3);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            animation: slideUp 1s ease;
        }
        
        @keyframes slideUp {
            from { transform: translateY(50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        
        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: clamp(2rem, 8vw, 4rem);
            color: #fff;
            text-align: center;
            margin-bottom: 1rem;
            text-shadow: 0 0 30px rgba(255,105,180,0.8);
        }
        
        .sorry-section {
            background: linear-gradient(135deg, #ff6b9d, #ff8a80);
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            margin-bottom: 2rem;
        }
        
        .sorry-section h2 {
            font-family: 'Dancing Script', cursive;
            font-size: clamp(1.8rem, 6vw, 3rem);
            color: #fff;
            margin-bottom: 1rem;
        }
        
        .love-messages {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin: 2rem 0;
        }
        
        .message {
            background: rgba(255,255,255,0.2);
            padding: 1.5rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border-left: 4px solid #ff69b4;
            animation: messagePop 0.6s ease forwards;
            opacity: 0;
        }
        
        .message:nth-child(1) { animation-delay: 0.1s; }
        .message:nth-child(2) { animation-delay: 0.2s; }
        .message:nth-child(3) { animation-delay: 0.3s; }
        .message:nth-child(4) { animation-delay: 0.4s; }
        
        @keyframes messagePop {
            from { transform: translateX(-50px); opacity: 0; }
            to { transform: translateX(0); opacity: 1; }
        }
        
        .games-section {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .game-card {
            background: rgba(255,255,255,0.2);
            border-radius: 20px;
            padding: 1.5rem;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .game-card:hover {
            transform: translateY(-10px);
            border-color: #ff69b4;
            box-shadow: 0 15px 30px rgba(255,105,180,0.4);
        }
        
        .proposal-btn {
            padding: 1.5rem 3rem;
            font-size: clamp(1.1rem, 4vw, 1.6rem);
            background: linear-gradient(45deg, #ff4081, #f50057);
            color: #fff;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 15px 35px rgba(255,64,129,0.5);
            transition: all 0.4s ease;
            font-family: 'Dancing Script', cursive;
            font-weight: 700;
            display: block;
            margin: 2rem auto 0;
        }
        
        .proposal-btn:hover {
            transform: scale(1.05) translateY(-5px);
            box-shadow: 0 25px 45px rgba(255,64,129,0.7);
        }
        
        /* Games */
        .game-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: rgba(0,0,0,0.8);
            display: none;
            justify-content: center;
            align-items: center;
            z-index: 100;
            backdrop-filter: blur(5px);
        }
        
        .game-content {
            background: rgba(255,255,255,0.95);
            border-radius: 25px;
            padding: 2rem;
            max-width: 90vw;
            max-height: 90vh;
            overflow: auto;
            color: #333;
            text-align: center;
        }
        
        .hearts-game {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1rem;
            max-width: 400px;
            margin: 0 auto;
        }
        
        .heart-btn {
            width: 60px;
            height: 60px;
            font-size: 2rem;
            border: none;
            border-radius: 15px;
            cursor: pointer;
            transition: all 0.3s ease;
            background: linear-gradient(135deg, #ff9a9e, #fecfef);
        }
        
        .heart-btn.matched {
            background: linear-gradient(135deg, #ff6b9d, #ff4081);
            transform: scale(1.1);
        }
        
        /* Mobile perfect */
        @media (max-width: 480px) {
            .container { padding: 1rem; }
            .games-section { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="hearts-bg" id="heartsBg"></div>
    
    <div class="container">
        <div class="card">
            <h1>💖 Sanskriti 💖</h1>
            <p style="font-size: clamp(1.1rem, 4vw, 1.4rem);">My dearest love, my everything...</p>
        </div>
        
        <div class="card sorry-section">
            <h2>I'm So Sorry 😔</h2>
            <p style="font-size: clamp(1rem, 3.5vw, 1.3rem); line-height: 1.6;">
                Sanskriti, please forgive me for hurting you. 
                <br>I promise to be better, to love you more fiercely every day.
                <br>You mean the world to me ❤️
            </p>
        </div>
        
        <div class="card">
            <h2>💕 Love Messages 💕</h2>
            <div class="love-messages">
                <div class="message">
                    "You make my heart smile brighter than the sun 🌞"
                </div>
                <div class="message">
                    "Every moment with you feels like a dream 💭"
                </div>
                <div class="message">
                    "You're my forever, my always, my everything ✨"
                </div>
                <div class="message">
                    "I love you more than words can express 💖"
                </div>
            </div>
        </div>
        
        <div class="card">
            <h2>🎮 Play With Me 🎮</h2>
            <div class="games-section">
                <div class="game-card" onclick="openGame('hearts')">
                    <div style="font-size: 3rem;">💕</div>
                    <h3>Match Hearts</h3>
                </div>
                <div class="game-card" onclick="openGame('memory')">
                    <div style="font-size: 3rem;">🧠</div>
                    <h3>Memory Game</h3>
                </div>
            </div>
        </div>
        
        <button class="proposal-btn" onclick="finalProposal()">
            💍 Forgive Me & Be Mine Forever? 💍
        </button>
    </div>
    
    <!-- Games Overlay -->
    <div class="game-overlay" id="gameOverlay">
        <div class="game-content">
            <h2 id="gameTitle"></h2>
            <div id="gameArea"></div>
            <button onclick="closeGame()" style="margin-top: 1rem; padding: 0.8rem 1.5rem; background: #ff69b4; color: white; border: none; border-radius: 25px; cursor: pointer;">Close ❤️</button>
        </div>
    </div>
    
    <script>
        // Floating hearts background
        const hearts = '💖💕💗💝🌸🌺🌹'.split('');
        for(let i = 0; i < 20; i++) {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.textContent = hearts[Math.floor(Math.random() * hearts.length)];
            heart.style.left = Math.random() * 100 + '%';
            heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
            heart.style.animationDelay = Math.random() * 2 + 's';
            document.getElementById('heartsBg').appendChild(heart);
        }
        
        // Love messages animation
        setTimeout(() => {
            document.querySelectorAll('.message').forEach(msg => {
                msg.style.opacity = '1';
            });
        }, 500);
        
        function openGame(type) {
            const overlay = document.getElementById('gameOverlay');
            const title = document.getElementById('gameTitle');
            const area = document.getElementById('gameArea');
            
            if(type === 'hearts') {
                title.textContent = '💕 Match the Hearts 💕';
                area.innerHTML = `
                    <div class="hearts-game" id="heartsGame">
                        <button class="heart-btn" data-match="1">💖</button>
                        <button class="heart-btn" data-match="1">💖</button>
                        <button class="heart-btn" data-match="2">💕</button>
                        <button class="heart-btn" data-match="2">💕</button>
                        <button class="heart-btn" data-match="3">💗</button>
                        <button class="heart-btn" data-match="3">💗</button>
                    </div>
                    <p>Click matching hearts! Perfect score for my perfect love 💕</p>
                `;
                document.querySelectorAll('.heart-btn').forEach(btn => {
                    btn.onclick = () => {
                        const match = btn.dataset.match;
                        document.querySelectorAll(`[data-match="${match}"]`).forEach(b => {
                            b.classList.add('matched');
                            b.disabled = true;
                        });
                    };
                });
            }
            
            overlay.style.display = 'flex';
        }
        
        function closeGame() {
            document.getElementById('gameOverlay').style.display = 'none';
        }
        
        function finalProposal() {
            alert('💖 Sanskriti, I love you forever! Will you forgive me and be mine? 💍');
            confetti();
        }
        
        // Simple confetti
        function confetti() {
            for(let i = 0; i < 50; i++) {
                const c = document.createElement('div');
                c.innerHTML = '💖';
                c.style.position = 'fixed';
                c.style.left = Math.random() * 100 + 'vw';
                c.style.top = '0';
                c.style.pointerEvents = 'none';
                c.style.fontSize = '20px';
                c.style.zIndex = '999';
                c.style.animation = 'fall 3s linear forwards';
                document.body.appendChild(c);
                setTimeout(() => c.remove(), 3000);
            }
        }
        
        // CSS for confetti
        const style = document.createElement('style');
        style.textContent = `
            @keyframes fall {
                to { transform: translateY(100vh) rotate(720deg); opacity: 0; }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>

