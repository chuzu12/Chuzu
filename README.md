<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Chuzu ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">

<style>
    :root {
        --primary-pink: #ff6f91;
        --soft-pink: #ffb6c1;
        --glass: rgba(255, 255, 255, 0.25);
    }

    body {
        margin: 0;
        padding: 0;
        font-family: 'Quicksand', sans-serif;
        background: url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg') no-repeat center center fixed;
        background-size: cover;
        height: 100vh;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        transition: background 1.5s ease-in-out;
    }

    /* Glassmorphism Container */
    .container {
        background: var(--glass);
        backdrop-filter: blur(12px);
        -webkit-backdrop-filter: blur(12px);
        border: 1px solid rgba(255, 255, 255, 0.3);
        padding: 40px;
        border-radius: 40px;
        box-shadow: 0 15px 35px rgba(0,0,0,0.15);
        text-align: center;
        max-width: 450px;
        width: 85%;
        z-index: 10;
        animation: slideUp 1s ease-out;
    }

    h1 { 
        font-family: 'Pacifico', cursive;
        font-size: 3.5rem; 
        color: white;
        margin: 0 0 10px 0;
        text-shadow: 2px 4px 6px rgba(0,0,0,0.1);
    }

    p { color: white; font-size: 1.1rem; font-weight: 600; margin: 5px 0; }

    .center-img {
        width: 100%;
        max-width: 260px;
        border: 12px solid #fff;
        border-bottom: 45px solid #fff;
        border-radius: 5px;
        margin: 25px auto;
        box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        display: block;
        transform: rotate(-2deg);
        transition: transform 0.5s ease;
    }

    .center-img:hover { transform: rotate(0deg) scale(1.05); }

    .btn-group {
        margin-top: 25px;
        display: flex;
        justify-content: center;
        gap: 20px;
        min-height: 60px; /* Prevents layout jump when No moves */
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

    .yes { background: var(--primary-pink); color: white; }
    .yes:hover { transform: scale(1.15); box-shadow: 0 12px 20px rgba(255, 111, 145, 0.4); }

    .no { 
        background: white; 
        color: var(--primary-pink); 
        position: relative; 
        z-index: 100;
    }

    /* Professional Animations */
    @keyframes slideUp {
        from { opacity: 0; transform: translateY(50px); }
        to { opacity: 1; transform: translateY(0); }
    }

    .heart {
        position: absolute;
        pointer-events: none;
        animation: floatUp 4s linear infinite;
        font-size: 20px;
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
    <h1>Chuzu ❤️</h1>
    <p>Every moment with you is a gift ✨</p>
    
    <img src="https://i.ibb.co/v6hMDR0W/1774992960985.png" alt="Our Moment" class="center-img">
    
    <p>Will you be mine forever? 💍</p>
    
    <div class="btn-group">
        <button class="yes" onclick="yesClicked()">Yes 😍</button>
        <button class="no" id="no-btn" onmouseover="dodgeButton()" onclick="dodgeButton()">No 😅</button>
    </div>
    
    <p style="font-size:14px; opacity:0.8; margin-top: 30px;">— Yours, Zairuu</p>
</div>

<script>
const noQuotes = [
    "Nice try! 😉", 
    "Not that easy! 🏃‍♂️", 
    "Wrong button! ❌", 
    "Are you sure? 🤨", 
    "Think again! 💎", 
    "Try the other one! 👉",
    "Catch me if you can! 💨"
];

function dodgeButton() {
    const btn = document.getElementById('no-btn');
    
    // Change text randomly
    const randomQuote = noQuotes[Math.floor(Math.random() * noQuotes.length)];
    btn.innerHTML = randomQuote;

    // Calculate random position
    // Ensure button stays within visible screen area
    const x = Math.random() * (window.innerWidth - btn.offsetWidth - 50);
    const y = Math.random() * (window.innerHeight - btn.offsetHeight - 50);
    
    btn.style.position = "fixed";
    btn.style.transition = "all 0.4s cubic-bezier(0.19, 1, 0.22, 1)"; // Smooth "zip" movement
    btn.style.left = x + "px";
    btn.style.top = y + "px";
}

function yesClicked() {
    // Reveal original photo as full background
    document.body.style.background = "linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('https://i.ibb.co/v6hMDR0W/1774992960985.png')";
    document.body.style.backgroundSize = "cover";
    document.body.style.backgroundPosition = "center";

    const card = document.getElementById('main-card');
    card.style.background = "rgba(255, 255, 255, 0.15)";
    card.innerHTML = `
        <h1 style="font-size: 4rem;">Yay!!! ❤️</h1>
        <p style="font-size: 1.5rem; margin-top: 20px;">You just made me the happiest man alive, Chuzu! 😍</p>
        <p style="margin-top: 15px;">I promise to cherish you every single day.</p>
        <div style="margin-top: 40px; font-family: 'Pacifico'; font-size: 2rem;">Zairuu ❤️</div>
    `;

    // Burst of hearts
    for(let i=0; i<50; i++) {
        setTimeout(createHeart, i * 50);
    }
}

function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = ["❤️", "💖", "💝", "💕"][Math.floor(Math.random() * 4)];
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (Math.random() * 2 + 3) + "s";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 5000);
}

// Initial subtle hearts
setInterval(createHeart, 600);
</script>

</body>
</html>
