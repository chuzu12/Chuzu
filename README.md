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
        --soft-pink: #ffb6c1;
    }

    body {
        margin: 0;
        padding: 0;
        font-family: 'Quicksand', sans-serif;
        /* Start with a clean, light romantic background */
        background: url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg') no-repeat center center fixed;
        background-size: cover;
        height: 100vh;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        transition: background 1.2s ease-in-out;
    }

    /* Professional Glassmorphism Container */
    .container {
        background: rgba(255, 255, 255, 0.25); /* Frosted glass effect */
        backdrop-filter: blur(12px);
        -webkit-backdrop-filter: blur(12px);
        border: 1px solid rgba(255, 255, 255, 0.4);
        padding: 40px;
        border-radius: 40px;
        box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        position: relative;
        z-index: 10;
        max-width: 420px;
        width: 85%;
        animation: slideUp 1s ease-out;
    }

    @keyframes slideUp {
        from { opacity: 0; transform: translateY(50px); }
        to { opacity: 1; transform: translateY(0); }
    }

    h1 { 
        font-family: 'Pacifico', cursive;
        font-size: 3.5rem; 
        color: #fff;
        margin: 0 0 15px 0;
        text-shadow: 2px 3px 6px rgba(0,0,0,0.1);
        letter-spacing: 2px;
    }

    p { color: #fff; font-size: 1.2rem; font-weight: 500; margin: 8px 0; }

    /* Centered, contained photo style for second page (Keepsake look) */
    .center-keepsake-img {
        width: 100%;
        max-width: 280px;
        height: auto;
        display: block;
        margin: 25px auto;
        border: 12px solid #fff;
        border-bottom: 40px solid #fff; /* Polaroid style */
        border-radius: 5px;
        box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        image-rendering: -webkit-optimize-contrast; 
        object-fit: contain;
    }

    .btn-group {
        margin-top: 30px;
        display: flex;
        justify-content: center;
        gap: 20px;
    }

    button {
        padding: 15px 35px;
        border: none;
        border-radius: 50px;
        font-size: 1.1rem;
        font-weight: 700;
        cursor: pointer;
        font-family: 'Quicksand', sans-serif;
        transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        box-shadow: 0 8px 15px rgba(0,0,0,0.1);
    }

    .yes { 
        background: var(--primary-pink); 
        color: white; 
    }
    .yes:hover { 
        transform: scale(1.1); 
        box-shadow: 0 12px 20px rgba(255, 111, 145, 0.3); 
    }

    .no { 
        background: white; 
        color: var(--primary-pink); 
        position: relative; 
        transition: all 0.2s ease;
    }

    /* Success Slide Appearance */
    .second-slide {
        display: none;
        animation: fadeIn 1.5s forwards;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }

    /* Decorative Romantic Stickers (Floating Elements) */
    .romantic-sticker {
        position: absolute;
        pointer-events: none;
        font-size: 25px;
        color: rgba(255, 111, 145, 0.8);
        animation: floatUp 4s linear infinite;
        opacity: 0.8;
        z-index: 1;
    }

    @keyframes floatUp {
        0% { transform: translateY(110vh) rotate(0deg); opacity: 1; }
        100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
    }

    /* Small sparkle stickers */
    .sparkle {
        font-size: 18px;
        color: #fff;
        position: absolute;
    }
</style>
</head>
<body>

<div class="container" id="main-card">
    <div id="slide1">
        <h1>AIMAN ❤️</h1>
        <p>You make my heart skip a beat... ✨</p>
        <p>Will you be mine forever? 💍</p>
        
        <div class="btn-group">
            <button class="yes" onclick="yesClicked()">Yes 😍</button>
            <button class="no" id="no-btn" onmouseover="dodgeButton()" onclick="dodgeButton()">No 😅</button>
        </div>
        
        <p style="font-size:14px; opacity:0.8; margin-top: 30px;">— Yours, Zairuu</p>
    </div>

    <div id="slide2" class="second-slide">
        <h1 style="font-size: 4rem;">Yay!!! ❤️</h1>
        <p style="font-size: 1.5rem; margin-top: 20px;">You just made me the happiest person alive, AIMAN! 😍</p>
        
        <img src="https://i.ibb.co/v6hMDR0W/1774992960985.png" alt="Our Promise" class="center-keepsake-img">
        
        <p style="margin-top: 15px;">I promise to cherish you every single day.</p>
        <div style="margin-top: 40px; font-family: 'Pacifico'; font-size: 2.2rem; color: #fff;">Zairuu ❤️</div>
    </div>
</div>

<script>
const noQuotes = [
    "Nice try! 😉", 
    "Wrong button! ❌", 
    "Try the other one! 👉",
    "Think again! 💎", 
    "Catch me if you can! 💨"
];

function dodgeButton() {
    const btn = document.getElementById('no-btn');
    const randomQuote = noQuotes[Math.floor(Math.random() * noQuotes.length)];
    btn.innerHTML = randomQuote;
    const x = Math.random() * (window.innerWidth - btn.offsetWidth - 50);
    const y = Math.random() * (window.innerHeight - btn.offsetHeight - 50);
    btn.style.position = "fixed";
    btn.style.transition = "all 0.4s cubic-bezier(0.19, 1, 0.22, 1)"; // Gliding movement
    btn.style.left = x + "px";
    btn.style.top = y + "px";
}

function yesClicked() {
    // Subtle background change with overlay for readability
    document.body.style.background = "linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('https://i.ibb.co/v6hMDR0W/1774992960985.png')";
    document.body.style.backgroundSize = "cover";
    document.body.style.backgroundPosition = "center";

    const card = document.getElementById('main-card');
    document.getElementById('slide1').style.display = 'none';
    document.getElementById('slide2').style.display = 'block';

    // Update card to Success appearance
    card.style.background = "rgba(0, 0, 0, 0.5)";

    // Launch celebratory burst of stickers
    for(let i=0; i<30; i++) {
        setTimeout(createSticker, i * 100);
    }
}

// Generates decorative, floating stickers/emojis
function createSticker() {
    const sticker = document.createElement("div");
    sticker.classList.add("romantic-sticker");
    sticker.innerHTML = ["❤️", "✨", "💍", "💕", "🥂"][Math.floor(Math.random() * 5)];
    sticker.style.left = Math.random() * 100 + "vw";
    sticker.style.animationDuration = (Math.random() * 2 + 3) + "s";
    sticker.style.fontSize = (Math.random() * 10 + 20) + "px";
    document.body.appendChild(sticker);
    setTimeout(() => sticker.remove(), 5000);
}

// Initial subtle stickers immediate ambiance
setInterval(createSticker, 900);
</script>

</body>
</html>
