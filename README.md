<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For AIMAN ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@500;700&display=swap" rel="stylesheet">

<style>
    :root {
        --primary-pink: #ff6f91;
        --glass-bg: rgba(255, 255, 255, 0.25);
    }

    body {
        margin: 0;
        padding: 0;
        font-family: 'Quicksand', sans-serif;
        /* First page background: Cute teddy theme */
        background: url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg') no-repeat center center fixed;
        background-size: cover;
        height: 100vh;
        width: 100vw;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        transition: background 1.5s ease-in-out;
    }

    .container {
        background: var(--glass-bg);
        backdrop-filter: blur(12px);
        -webkit-backdrop-filter: blur(12px);
        border: 1px solid rgba(255, 255, 255, 0.3);
        padding: 40px;
        border-radius: 40px;
        box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        position: relative;
        z-index: 10;
        max-width: 450px;
        width: 85%;
        animation: slideUp 0.8s ease-out;
    }

    @keyframes slideUp {
        from { opacity: 0; transform: translateY(40px); }
        to { opacity: 1; transform: translateY(0); }
    }

    h1 { 
        font-family: 'Pacifico', cursive;
        font-size: 3rem; 
        color: #fff;
        margin: 0 0 10px 0;
        text-shadow: 2px 3px 6px rgba(0,0,0,0.2);
        letter-spacing: 2px;
    }

    p { color: #fff; font-size: 1.2rem; font-weight: 600; margin: 10px 0; }

    /* Hugging Teddy GIF on Page 1 */
    .teddy-hug-gif {
        width: 100%;
        max-width: 220px;
        height: auto;
        display: block;
        margin: 20px auto;
        border-radius: 20px;
        filter: drop-shadow(0 5px 15px rgba(0,0,0,0.1));
    }

    /* Second Page Polaroid Photo: Centered & Sharp */
    .center-keepsake {
        width: 100%;
        max-width: 280px;
        height: auto;
        display: block;
        margin: 25px auto;
        border: 12px solid #fff;
        border-bottom: 45px solid #fff; /* Polaroid style */
        border-radius: 4px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        /* Sharpness Fix */
        image-rendering: -webkit-optimize-contrast;
        object-fit: contain;
    }

    .btn-group {
        margin-top: 30px;
        display: flex;
        justify-content: center;
        gap: 20px;
        min-height: 70px;
    }

    button {
        padding: 15px 35px;
        border: none;
        border-radius: 50px;
        font-size: 1.1rem;
        font-weight: 700;
        cursor: pointer;
        font-family: 'Quicksand', sans-serif;
        box-shadow: 0 8px 15px rgba(0,0,0,0.1);
        transition: transform 0.2s ease;
    }

    .yes { background: var(--primary-pink); color: white; }
    .yes:hover { transform: scale(1.1); }

    .no { 
        background: #fff; 
        color: var(--primary-pink); 
        position: relative;
        transition: all 0.3s cubic-bezier(0.19, 1, 0.22, 1);
        white-space: nowrap;
    }

    #slide2 { display: none; }

    .heart {
        position: absolute;
        pointer-events: none;
        animation: floatUp 4s linear infinite;
        z-index: 1;
    }

    @keyframes floatUp {
        0% { transform: translateY(110vh) rotate(0deg); opacity: 1; }
        100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
    }
</style>
</head>
<body>

<div class="container" id="main-card">
    <div id="slide1">
        <h1>AIMAN ❤️</h1>
        <p>You make every day feel like a hug... ✨</p>
        
        <img src="https://i.ibb.co/XzC8fFm/teddy-hug.gif" alt="Teddy Hug" class="teddy-hug-gif">
        
        <p>Will you be mine forever? 💍</p>
        
        <div class="btn-group">
            <button class="yes" onclick="yesClicked()">Yes 😍</button>
            <button class="no" id="no-btn" onmouseover="moveNo()" ontouchstart="moveNo()">No 😅</button>
        </div>
        <p style="font-size:14px; opacity:0.9; margin-top: 25px;">— Forever Yours, Zairuu</p>
    </div>

    <div id="slide2">
        <h1 style="font-size: 3.5rem;">YAY!!! ❤️</h1>
        <p style="font-size: 1.4rem;">You've made me the happiest alive, AIMAN! 😍</p>
        
        <img src="https://i.ibb.co/BpDLXMb/1774992960985.png" alt="Our Promise" class="center-keepsake">
        
        <p>I promise to hold your hand through everything.</p>
        <div style="margin-top: 35px; font-family: 'Pacifico'; font-size: 2.2rem; color: #fff;">Zairuu ❤️</div>
    </div>
</div>

<script>
const quotes = ["Are you sure? 🤨", "Nice try! 😉", "Wrong button! ❌", "Try again! ✨", "Not today! 🏃‍♀️", "Catch me! 💨"];

function moveNo() {
    const btn = document.getElementById('no-btn');
    btn.innerHTML = quotes[Math.floor(Math.random() * quotes.length)];
    
    const padding = 50;
    const maxX = window.innerWidth - btn.offsetWidth - padding;
    const maxY = window.innerHeight - btn.offsetHeight - padding;
    
    const randomX = Math.max(padding, Math.floor(Math.random() * maxX));
    const randomY = Math.max(padding, Math.floor(Math.random() * maxY));
    
    btn.style.position = "fixed";
    btn.style.left = randomX + "px";
    btn.style.top = randomY + "px";
}

function yesClicked() {
    // Reveal Slide 2
    document.getElementById('slide1').style.display = 'none';
    document.getElementById('slide2').style.display = 'block';
    
    // Background transition to a more romantic overlay
    document.body.style.background = "linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg')";
    document.body.style.backgroundSize = "cover";
    document.getElementById('main-card').style.background = "rgba(0, 0, 0, 0.6)";

    // Heart celebration
    for(let i=0; i<50; i++) { 
        setTimeout(createHeart, i * 70); 
    }
}

function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = ["❤️", "💖", "💝", "💕"][Math.floor(Math.random() * 4)];
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (Math.random() * 2 + 3) + "s";
    heart.style.fontSize = (Math.random() * 15 + 15) + "px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 4000);
}

// Background hearts
setInterval(createHeart, 1000);
</script>

</body>
</html>
