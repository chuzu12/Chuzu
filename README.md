<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Aiman ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@500;700&display=swap" rel="stylesheet">

<style>
    body {
        margin: 0;
        padding: 0;
        font-family: 'Quicksand', sans-serif;
        /* Using a gradient background for a professional touch that looks good on mobile and desktop */
        background: linear-gradient(135deg, #fdfbfb 0%, #ebedee 100%);
        height: 100vh;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        transition: background 1.5s ease-in-out;
    }

    .container {
        /* Soft, semi-transparent pink panel */
        background: rgba(255, 192, 203, 0.6);
        padding: 40px;
        border-radius: 35px;
        box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        position: relative;
        z-index: 10;
        max-width: 420px;
        width: 90%;
        backdrop-filter: blur(5px);
        animation: slideIn 1s ease-out;
    }

    /* Professional fade-in animation */
    @keyframes slideIn {
        from { opacity: 0; transform: translateY(30px); }
        to { opacity: 1; transform: translateY(0); }
    }

    h1 { 
        font-family: 'Pacifico', cursive;
        font-size: 3.2em; 
        color: #fff;
        margin: 0 0 15px 0;
        text-shadow: 2px 3px 6px rgba(0,0,0,0.1);
    }

    p { color: #fff; font-size: 1.2em; font-weight: 500; margin: 8px 0; }

    /* The Center Image: Clean, Sharp, and Centered */
    .center-img {
        width: 100%;
        max-width: 280px;
        height: auto;
        display: block;
        margin: 25px auto;
        border: 10px solid #fff;
        border-bottom: 40px solid #fff; /* Polaroid effect */
        border-radius: 5px;
        box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        /* CSS to ensure image is not blurry on high-res screens */
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
        font-size: 1.1em;
        font-weight: 700;
        cursor: pointer;
        transition: all 0.3s ease;
        font-family: 'Quicksand', sans-serif;
        box-shadow: 0 8px 15px rgba(0,0,0,0.1);
    }

    .yes { 
        background: #ff6f91; 
        color: white; 
    }
    .yes:hover { 
        transform: scale(1.1); 
        box-shadow: 0 12px 20px rgba(255, 111, 145, 0.3); 
    }

    .no { 
        background: white; 
        color: #ff6f91; 
        position: relative; 
        transition: all 0.2s ease;
    }

    /* The "No" button move animation will be applied via JS */

    /* Hearts */
    .heart {
        position: absolute;
        pointer-events: none;
        animation: floatUp 4s linear infinite;
        opacity: 0.8;
    }

    @keyframes floatUp {
        0% { transform: translateY(110vh) rotate(0deg); opacity: 1; }
        100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
    }
</style>
</head>
<body>

<div class="container" id="main-card">
    <h1>Aiman ❤️</h1>
    <p>Every moment with you is special ✨</p>
    
    <img src="https://i.ibb.co/v6hMDR0W/1774992960985.png" alt="Our Moment" class="center-img">
    
    <p>Will you be mine forever? 💍</p>
    
    <div class="btn-group">
        <button class="yes" onclick="yesClicked()">Yes 😍</button>
        <button class="no" id="no-btn" onmouseover="dodgeButton()" onclick="dodgeButton()">No 😅</button>
    </div>
    
    <p style="font-size:14px; opacity:0.8; margin-top: 30px;">— Your Zairuu</p>
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
    
    // Change text randomly to add to the fun
    const randomQuote = noQuotes[Math.floor(Math.random() * noQuotes.length)];
    btn.innerHTML = randomQuote;

    // Calculate a random position that keeps the button on screen
    const x = Math.random() * (window.innerWidth - btn.offsetWidth - 50);
    const y = Math.random() * (window.innerHeight - btn.offsetHeight - 50);
    
    btn.style.position = "fixed";
    // Smooth, gliding transition for a pro feel
    btn.style.transition = "all 0.4s cubic-bezier(0.19, 1, 0.22, 1)";
    btn.style.left = x + "px";
    btn.style.top = y + "px";
}

function yesClicked() {
    // Background changes to a subtle romantic color
    document.body.style.background = "linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('https://i.ibb.co/v6hMDR0W/1774992960985.png')";
    document.body.style.backgroundSize = "cover";
    document.body.style.backgroundPosition = "center";

    const card = document.getElementById('main-card');
    // Darken the card overlay to make white text pop against the background
    card.style.background = "rgba(0, 0, 0, 0.4)";
    card.innerHTML = `
        <h1 style="font-size: 3.5rem;">Yay!!! ❤️</h1>
        <p style="font-size: 1.5rem; margin-top: 20px;">You just made me the happiest man alive, Aiman! 😍</p>
        <p style="margin-top: 15px;">I promise to cherish you every single day.</p>
        <div style="margin-top: 40px; font-family: 'Pacifico'; font-size: 2rem; color: #fff;">Zairuu ❤️</div>
    `;

    // A burst of hearts for celebration
    for(let i=0; i<30; i++) {
        setTimeout(createHeart, i * 100);
    }
}

function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    // Mix of heart emojis
    heart.innerHTML = ["❤️", "💖", "💝", "💕"][Math.floor(Math.random() * 4)];
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (Math.random() * 2 + 3) + "s";
    heart.style.fontSize = (Math.random() * 10 + 15) + "px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 5000);
}

// Start with some subtle hearts immediately
setInterval(createHeart, 800);
</script>

</body>
</html>
