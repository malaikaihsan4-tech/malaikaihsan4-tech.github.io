
<html>
<head>
    <title>Do You Love Me? 💕</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Playfair+Display:wght@400;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            width: 100vw;
            height: 100vh;
            overflow: hidden;
            background: linear-gradient(145deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Poppins', sans-serif;
            position: relative;
        }
        
        /* Animated background particles */
        body::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            background-image: radial-gradient(circle at 20% 50%, rgba(255,255,255,0.05) 2%, transparent 2.5%);
            background-size: 40px 40px;
            animation: floatBackground 20s linear infinite;
        }
        
        @keyframes floatBackground {
            0% { transform: translateY(0); }
            100% { transform: translateY(-40px); }
        }
        
        .container {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(20px);
            border-radius: 30px;
            padding: 50px 60px;
            text-align: center;
            box-shadow: 0 25px 45px rgba(0,0,0,0.3), 0 0 0 1px rgba(255,255,255,0.05);
            width: 90%;
            max-width: 750px;
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.4s ease;
        }
        
        h1 {
            font-family: 'Playfair Display', 'Dancing Script', serif;
            font-size: 54px;
            margin-bottom: 45px;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 700;
            letter-spacing: 1px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .buttons {
            display: flex;
            gap: 35px;
            justify-content: center;
            align-items: center;
            margin-bottom: 45px;
        }
        
        .btn {
            border: none;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
            font-family: 'Poppins', sans-serif;
            letter-spacing: 0.5px;
            position: relative;
            overflow: hidden;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            border-radius: 50%;
            background: rgba(255,255,255,0.3);
            transform: translate(-50%, -50%);
            transition: width 0.6s, height 0.6s;
        }
        
        .btn:hover::before {
            width: 300px;
            height: 300px;
        }
        
        #yesBtn {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            font-size: 28px;
            padding: 16px 42px;
            border-radius: 50px;
            font-weight: 600;
            box-shadow: 0 8px 20px rgba(245,87,108,0.3);
        }
        
        #noBtn {
            background: rgba(255,255,255,0.08);
            backdrop-filter: blur(10px);
            color: rgba(255,255,255,0.8);
            font-size: 24px;
            padding: 14px 38px;
            border-radius: 50px;
            border: 1px solid rgba(255,255,255,0.2);
            font-weight: 500;
        }
        
        .quote-box {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(10px);
            padding: 28px;
            border-radius: 25px;
            min-height: 130px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            color: rgba(255,255,255,0.9);
            line-height: 1.5;
            font-weight: 400;
            font-family: 'Dancing Script', 'Playfair Display', cursive;
            border: 1px solid rgba(255,255,255,0.1);
            transition: all 0.3s ease;
            letter-spacing: 0.5px;
        }
        
        .heart {
            display: inline-block;
            animation: gentleBeat 2s ease-in-out infinite;
        }
        
        @keyframes gentleBeat {
            0%, 100% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.08); opacity: 1; }
        }
        
        .floating-heart {
            position: fixed;
            pointer-events: none;
            font-size: 20px;
            animation: elegantFloat 4s ease-out forwards;
            z-index: 10000;
            opacity: 0.7;
        }
        
        @keyframes elegantFloat {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0.7;
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* Premium glow effect on YES button */
        @keyframes premiumGlow {
            0%, 100% { box-shadow: 0 8px 20px rgba(245,87,108,0.3); }
            50% { box-shadow: 0 8px 30px rgba(245,87,108,0.6); }
        }
        
        #yesBtn {
            animation: premiumGlow 3s ease-in-out infinite;
        }
        
        @media (max-width: 600px) {
            .container {
                padding: 35px 30px;
            }
            h1 {
                font-size: 38px;
                margin-bottom: 35px;
            }
            #yesBtn {
                font-size: 22px;
                padding: 12px 32px;
            }
            #noBtn {
                font-size: 20px;
                padding: 10px 28px;
            }
            .quote-box {
                font-size: 20px;
                padding: 20px;
                min-height: 110px;
            }
            .buttons {
                gap: 25px;
                margin-bottom: 35px;
            }
        }
        
        @media (max-height: 700px) {
            .container {
                padding: 35px 50px;
            }
            h1 {
                font-size: 44px;
                margin-bottom: 30px;
            }
            .quote-box {
                padding: 22px;
                min-height: 110px;
                font-size: 22px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>
            <span class="heart">💕</span> 
            Do You Love Me? 
            <span class="heart">💕</span>
        </h1>
        
        <div class="buttons">
            <button class="btn" id="yesBtn">YES</button>
            <button class="btn" id="noBtn">NO</button>
        </div>
        
        <div class="quote-box" id="quoteBox">
            ✨ Tell me the truth... ✨
        </div>
    </div>

    <script>
        const yesBtn = document.getElementById('yesBtn');
        const noBtn = document.getElementById('noBtn');
        const quoteBox = document.getElementById('quoteBox');
        
        let noCount = 0;
        let yesUnlocked = false;
        
        const loveQuotes = [
            "💕 I love you forever and always 💕",
            "🌸 You mean everything to me 🌸",
            "💖 My heart beats only for you 💖",
            "🌟 You are my sunshine 🌟",
            "💝 Every day I love you more 💝",
            "🎀 You are my dream come true 🎀",
            "✨ Forever and ever, I love you ✨",
            "💗 You make my world complete 💗",
            "🌹 I fall in love with you every day 🌹",
            "💕 You are my one and only 💕",
            "😊 Your smile is my happiness 😊",
            "💫 I will love you until the end of time 💫",
            "🎈 You are my everything 🎈",
            "💓 Loving you is the best thing I've ever done 💓",
            "⭐ You are my greatest adventure ⭐",
            "💖 I love you more than all the stars in the sky 💖",
            "🌸 You are my forever and always 🌸",
            "💕 My love for you grows stronger every second 💕",
            "🌟 You are the reason I believe in love 🌟",
            "💝 I will never stop loving you 💝",
            "❤️ Every breath I take is for you ❤️",
            "💗 You are my soulmate forever 💗",
            "🌙 I dream of you every night 🌙",
            "☀️ You are my first thought every morning ☀️"
        ];
        
        function showLoveQuote() {
            const randomIndex = Math.floor(Math.random() * loveQuotes.length);
            quoteBox.innerHTML = loveQuotes[randomIndex];
        }
        
        function createFloatingHeart() {
            const heart = document.createElement('div');
            heart.innerHTML = ['❤️', '💕', '💖', '💗', '💓', '💝', '💘'][Math.floor(Math.random() * 7)];
            heart.className = 'floating-heart';
            heart.style.left = Math.random() * window.innerWidth + 'px';
            heart.style.bottom = '-20px';
            heart.style.fontSize = (18 + Math.random() * 30) + 'px';
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 4000);
        }
        
        function makeNoButtonRun() {
            const maxX = window.innerWidth - noBtn.offsetWidth - 50;
            const maxY = window.innerHeight - noBtn.offsetHeight - 80;
            const randomX = Math.random() * maxX;
            const randomY = Math.random() * maxY;
            
            noBtn.style.position = 'fixed';
            noBtn.style.left = randomX + 'px';
            noBtn.style.top = randomY + 'px';
            noBtn.style.transition = 'all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1)';
        }
        
        document.addEventListener('mousemove', (e) => {
            if (yesUnlocked) {
                const btnRect = noBtn.getBoundingClientRect();
                const distance = Math.hypot(e.clientX - (btnRect.left + btnRect.width/2), 
                                           e.clientY - (btnRect.top + btnRect.height/2));
                if (distance < 100) {
                    makeNoButtonRun();
                }
            }
        });
        
        noBtn.onclick = () => {
            noCount++;
            showLoveQuote();
            
            for(let i = 0; i < 3; i++) {
                setTimeout(() => createFloatingHeart(), i * 100);
            }
            
            let newSize = 28 + (noCount * 1.5);
            yesBtn.style.fontSize = Math.min(newSize, 52) + 'px';
            yesBtn.style.padding = (16 + noCount * 0.8) + 'px ' + (42 + noCount * 1.5) + 'px';
            
            let noSize = Math.max(24 - noCount * 0.5, 14);
            noBtn.style.fontSize = noSize + 'px';
            noBtn.style.padding = (14 - noCount * 0.3) + 'px ' + (38 - noCount * 0.8) + 'px';
            
            if (noCount >= 12 && !yesUnlocked) {
                yesUnlocked = true;
                quoteBox.innerHTML = "💕 I've been waiting for this moment... 💕";
                setTimeout(() => showLoveQuote(), 1500);
            }
            
            if (yesUnlocked) {
                makeNoButtonRun();
            }
        };
        
        yesBtn.onclick = () => {
            if (!yesUnlocked) {
                showLoveQuote();
                yesBtn.style.transform = 'scale(0.97)';
                setTimeout(() => yesBtn.style.transform = 'scale(1)', 300);
            } else {
                for(let i = 0; i < 60; i++) {
                    setTimeout(() => createFloatingHeart(), i * 40);
                }
                
                document.body.style.background = 'linear-gradient(145deg, #f093fb 0%, #f5576c 50%, #f093fb 100%)';
                document.querySelector('.container').style.background = 'rgba(255, 255, 255, 0.1)';
                document.querySelector('.container').style.backdropFilter = 'blur(30px)';
                
                quoteBox.innerHTML = "💖💖💖 I LOVE YOU TOO! FOREVER AND ALWAYS! 💖💖💖";
                quoteBox.style.fontSize = "28px";
                quoteBox.style.background = 'rgba(255,255,255,0.15)';
                quoteBox.style.border = '1px solid rgba(255,255,255,0.3)';
                quoteBox.style.color = 'white';
                
                noBtn.disabled = true;
                noBtn.style.opacity = '0.2';
                noBtn.style.cursor = 'not-allowed';
                noBtn.style.position = 'relative';
                
                yesBtn.innerHTML = '❤️ I LOVE YOU FOREVER ❤️';
                yesBtn.style.fontSize = '36px';
                yesBtn.disabled = true;
                yesBtn.style.animation = 'none';
                
                setTimeout(() => {
                    alert('💖 I LOVE YOU! FOREVER AND EVER! 💖');
                }, 500);
            }
        };
        
        yesBtn.onmouseenter = () => {
            if (!yesUnlocked) {
                yesBtn.style.transform = 'scale(1.02)';
            } else {
                yesBtn.style.transform = 'scale(1.06)';
            }
        };
        
        yesBtn.onmouseleave = () => {
            yesBtn.style.transform = 'scale(1)';
        };
        
        window.addEventListener('resize', () => {
            if (yesUnlocked) {
                makeNoButtonRun();
            }
        });
    </script>
</body>
</html>

