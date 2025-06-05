<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Manisha  - My Valentine</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet" />
<style>
    /* Global Styles */
    body {
        margin: 0;
        background: linear-gradient(135deg, #ffdde1 0%, #ee9ca7 100%);
        font-family: 'Poppins', sans-serif;
        font-weight: 300;
        font-size: 14px;
        color: #331a1a;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        min-height: 100vh;
        overflow-x: hidden;
        user-select: none;
        padding: 20px;
        position: relative;
    }
    h1 {
        font-size: 1.8rem;
        font-weight: 600;
        margin-bottom: 0.5rem;
        line-height: 1.2;
    }
    button {
        font-family: 'Poppins', sans-serif;
        font-weight: 600;
        font-size: 1rem;
        padding: 10px 24px;
        margin: 12px 16px;
        border: none;
        border-radius: 25px;
        background: linear-gradient(45deg, #ff4b1f, #ff9068);
        color: white;
        cursor: pointer;
        box-shadow: 0 4px 8px rgba(255,75,31, 0.6);
        transition: transform 0.2s ease, box-shadow 0.2s ease;
        user-select: none;
    }
    button:hover {
        transform: scale(1.1);
        box-shadow: 0 6px 12px rgba(255,75,31, 0.8);
    }
    button:focus {
        outline: none;
        box-shadow: 0 0 0 3px #ffb6a5;
    }
    .hidden {
        display: none;
    }
    .emoji {
        font-size: 3rem;
        margin: 15px 0 30px 0;
        user-select: none;
        filter: drop-shadow(1px 1px 1px rgba(0,0,0,0.1));
        animation: bounce 2s infinite ease-in-out;
    }
    @keyframes bounce {
        0%, 100% { transform: translateY(0); }
        50% { transform: translateY(-10px); }
    }
    .small-text {
        font-size: 0.75rem;
        position: absolute;
        top: 12px;
        right: 12px;
        color: #5c1a1a;
        font-weight: 500;
        letter-spacing: 1px;
        user-select: none;
        opacity: 0.7;
    }
    .gift {
        font-weight: 600;
        margin: 8px 0;
        font-size: 1.1rem;
        user-select: none;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
    }
    .gift > span {
        font-size: 2rem;
    }
    #gameArea {
        margin-top: 20px;
    }
    #heart {
        font-size: 4rem;
        cursor: pointer;
        user-select: none;
        transition: transform 0.2s ease;
    }
    #heart:hover {
        transform: scale(1.2);
    }
    #score {
        font-weight: 600;
        margin-top: 10px;
        font-size: 1.2rem;
        color: #a32a2a;
        font-style: italic;
        user-select: none;
    }
    /* Swan animation container */
    #page10 {
        position: relative;
        width: 100%;
        max-width: 400px;
        height: 320px;
        overflow: hidden;
        background: linear-gradient(to bottom, #a0c9f0, #3874cb);
        border-radius: 20px;
        box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        color: #f1e7f0;
        font-weight: 600;
        padding: 10px;
    }
    /* Swan images container */
    #swans {
        position: absolute;
        bottom: 40px;
        width: 100%;
        height: 120px;
        overflow: visible;
        user-select: none;
    }
    .swan {
        position: absolute;
        bottom: 0;
        width: 120px;
        height: 120px;
        background: url('https://i.imgur.com/TapvrxX.png') no-repeat center/contain;
        filter: drop-shadow(0 0 8px #94738c88);
        animation-timing-function: ease-in-out;
    }
    #swan1 {
        left: -140px;
        transform: scaleX(1);
        animation: swanMove1 15s infinite alternate;
    }
    #swan2 {
        right: -140px;
        transform: scaleX(-1);
        animation: swanMove2 15s infinite alternate;
    }
    @keyframes swanMove1 {
        0% { left: -140px; bottom: 0; }
        50% { left: 130px; bottom: 40px; }
        100% { left: -140px; bottom: 0; }
    }
    @keyframes swanMove2 {
        0% { right: -140px; bottom: 0; }
        50% { right: 130px; bottom: 40px; }
        100% { right: -140px; bottom: 0; }
    }
    #iLoveYouText {
        position: absolute;
        bottom: 10px;
        right: 14px;
        font-size: 0.85rem;
        color: #ffe3e3;
        font-style: italic;
        text-shadow: 0 0 8px #ff7569;
        user-select: none;
        font-weight: 600;
        letter-spacing: 0.7px;
    }
    /* Navigation buttons container */
    .nav-buttons {
        margin-top: 30px;
        user-select: none;
    }
    .nav-buttons button {
        min-width: 100px;
    }
</style>
</head>
<body>

<div class="small-text" aria-label="Page author and version information" title="Page author and version">mr coder 2.0</div>
 
<!-- Page 1 -->
<div id="page1">
    <h1>💌 , Manisha💖  will you become my valentine? 💖</h1>
    <button id="yesBtn" title="Yes, I love you" aria-label="Yes, I love you button" onclick="nextPage(1)">Yes (I love you) ❤️</button>
    <button id="noBtn" title="No, I don't" aria-label="No, I don't button" onclick="noResponse()">No (I don't 😗)</button>
    <div class="nav-buttons">
      <!-- No previous button on first page -->
    </div>
</div>

<!-- Page 2 -->
<div id="page2" class="hidden">
    <h1>🎉 Now you are my valentine! I am happy! 😊</h1>
    <div class="emoji" aria-label="Dancing cat emoji">🐱‍👤🐱‍🏍🐱‍👓</div>
    <div class="nav-buttons">
        <button onclick="previousPage(2)">⬅️ Previous</button>
        <button onclick="nextPage(2)">Next ➡️</button>
    </div>
</div>

<!-- Page 3 -->
<div id="page3" class="hidden">
    <h1>🎁 Here is your gift! I hope this will make you happy! 🌟</h1>
    <div class="nav-buttons">
        <button onclick="previousPage(3)">⬅️ Previous</button>
        <button onclick="nextPage(3)">Next ➡️</button>
    </div>
</div>

<!-- Page 4 -->
<div id="page4" class="hidden">
    <h1>🎀 Gifts for you 🎀</h1>
    <div class="gift"><span>🧸</span> Cute Teddy Bear</div>
    <div class="gift"><span>💄</span> Box of Makeup</div>
    <div class="gift"><span>🍫</span> Chocolate Box</div>
    <div class="gift"><span>🎶</span> Music Playlist</div>
    <div class="gift"><span>🌹</span> Fresh Roses</div>
    <div class="nav-buttons">
        <button onclick="previousPage(4)">⬅️ Previous</button>
        <button onclick="nextPage(4)">Next ➡️</button>
    </div>
</div>

<!-- Page 5 -->
<div id="page5" class="hidden">
    <h1>💭 When I met you for the first time, I felt feelings that can't be described in words. ✨</h1>
    <div class="nav-buttons">
        <button onclick="previousPage(5)">⬅️ Previous</button>
        <button onclick="nextPage(5)">Next ➡️</button>
    </div>
</div>

<!-- Page 6 -->
<div id="page6" class="hidden">
    <h1>❓ I want to ask you, do you love me or not? 💘</h1>
    <button onclick="nextPage(6)">Yes, I really love you ❤️</button>
    <button onclick="destroyEarthquake()" style="background: linear-gradient(45deg, #a80000, #ff0000);">No, I hate you 😡</button>
    <div class="nav-buttons" style="margin-top: 15px;">
        <button onclick="previousPage(6)">⬅️ Previous</button>
        <!-- No next button since nextPage(6) leads to page 7 -->
    </div>
</div>

<!-- Page 7 -->
<div id="page7" class="hidden">
    <h1>🎉 If you are seeing this message, then you clicked on Yes! 💕</h1>
    <div class="nav-buttons">
        <button onclick="previousPage(7)">⬅️ Previous</button>
        <button onclick="nextPage(7)">Next ➡️</button>
    </div>
</div>

<!-- Page 8 -->
<div id="page8" class="hidden" style="padding: 0 20px;">
    <h1>🌹 Love is a beautiful feeling that connects two souls. It is the essence of life, bringing joy, happiness, and a sense of belonging. ❤️</h1>
    <div class="nav-buttons">
        <button onclick="previousPage(8)">⬅️ Previous</button>
        <button onclick="nextPage(8)">Next ➡️</button>
    </div>
</div>

<!-- Page 9 -->
<div id="page9" class="hidden">
    <h1>🎯 Game: Try to click the heart as many times as you can in 10 seconds! 💓</h1>
    <button onclick="startGame()">Start Game</button>
    <div id="gameArea" class="hidden" aria-live="polite" aria-atomic="true">
        <div id="heart" role="button" tabindex="0" aria-label="Heart to click">❤️</div>
        <div id="score">Score: 0</div>
    </div>
    <div class="nav-buttons" style="margin-top:30px;">
        <button onclick="previousPage(9)">⬅️ Previous</button>
        <button onclick="nextPage(9)">Next ➡️</button>
    </div>
</div>

<!-- Page 10 -->
<div id="page10" class="hidden">
    <h1>🦢 Two swans staring at each other on the water... 🌅</h1>
    <div id="swans" aria-label="Two swans moving on water">
        <div id="swan1" class="swan" aria-hidden="true"></div>
        <div id="swan2" class="swan" aria-hidden="true"></div>
    </div>
    <div id="iLoveYouText">I love you Anushka ❤️</div>
    <div class="nav-buttons" style="margin-top: 30px;">
        <button onclick="previousPage(10)">⬅️ Previous</button>
        <!-- No next button on last page -->
    </div>
</div>

<script>
    let currentPage = 1;
    let score = 0;
    let noBtn = document.getElementById('noBtn');
    let yesBtn = document.getElementById('yesBtn');

    function noResponse() {
        if (currentPage === 1) {
            // Move "No" button to a random position relative to "Yes" button
            const offsetX = (Math.random() * 140) - 70; // -70 to 70 px
            const offsetY = (Math.random() * 70) - 35; // -35 to 35 px
            noBtn.style.position = 'relative';
            noBtn.style.left = offsetX + 'px';
            noBtn.style.top = offsetY + 'px';
        } else if (currentPage === 6) {
            destroyEarthquake();
        }
    }

    function nextPage(page) {
        // Safety boundary for pages 1 to 10
        let next = page + 1;
        if (next > 10) next = 10;
        document.getElementById(`page${currentPage}`).classList.add('hidden');
        currentPage = next;
        document.getElementById(`page${currentPage}`).classList.remove('hidden');
    }

    function previousPage(page) {
        let prev = page - 1;
        if (prev < 1) prev = 1;
        document.getElementById(`page${currentPage}`).classList.add('hidden');
        currentPage = prev;
        document.getElementById(`page${currentPage}`).classList.remove('hidden');
        // Reset noBtn button position for page 1
        if(currentPage === 1) {
          noBtn.style.position = 'static';
          noBtn.style.left = '0';
          noBtn.style.top = '0';
        }
    }

    function destroyEarthquake() {
        const duration = 6000; 
        let startTime = null;
        const amplitude = 15;
        const body = document.body;

        function shake(timestamp) {
            if (!startTime) startTime = timestamp;
            let elapsed = timestamp - startTime;
            if (elapsed < duration) {
                const x = (Math.random() * amplitude * 2) - amplitude;
                const y = (Math.random() * amplitude * 2) - amplitude;
                body.style.transform = `translate(${x}px, ${y}px) rotate(${x}deg)`;
                requestAnimationFrame(shake);
            } else {
                body.style.transform = `translate(0,0) rotate(0)`;
                body.innerHTML = '<h1 style="color: crimson; font-weight: 700; font-family:\'Poppins\', sans-serif;">🌍 Earthquake! The page has crashed! 💥</h1>';
            }
        }

        requestAnimationFrame(shake);
    }

    function startGame() {
        score = 0;
        document.getElementById('score').innerText = "Score: 0";
        document.getElementById('gameArea').classList.remove('hidden');
        const heart = document.getElementById('heart');

        function incrementScore() {
            score++;
            document.getElementById('score').innerText = "Score: " + score;
            const gameArea = document.getElementById('gameArea');
            const maxX = gameArea.clientWidth - heart.clientWidth;
            const maxY = 200; 
            const randX = Math.floor(Math.random() * maxX);
            const randY = Math.floor(Math.random() * maxY);
            heart.style.position = 'relative';
            heart.style.left = randX + 'px';
            heart.style.top = randY + 'px';
        }

        heart.onclick = incrementScore;
        heart.onkeydown = function(e) {
            if (e.key === 'Enter' || e.key === ' ') {
                e.preventDefault();
                incrementScore();
            }
        };
        heart.setAttribute('tabindex','0');

        setTimeout(() => {
            alert(`Game over! Your score is: ${score} 💖`);
            // move to next page after game, which is page 10
            document.getElementById(`page${currentPage}`).classList.add('hidden');
            currentPage = 10;
            document.getElementById(`page${currentPage}`).classList.remove('hidden');
        }, 10000);
    }
</script>

</body>
</html>

 
