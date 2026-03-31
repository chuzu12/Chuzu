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
        background: url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg') no-repeat center center fixed;
        background-size: cover;
        height: 100vh;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        transition: background 1s ease-in-out;
    }

    /* Modern Glassmorphism Card */
    .container {
        background: rgba(255, 255, 255, 0.3); /* Frosted glass effect */
        backdrop-filter: blur(10px);
        -webkit-backdrop-filter: blur(10px);
        border: 1px solid rgba(255, 255, 255, 0.4);
        padding: 40px;
        border-radius: 40px;
        box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        position: relative;
        z-index: 10;
        max-width: 450px;
        width: 85%;
        animation: slideUp 1s ease-out;
    }

    @keyframes slideUp {
        from { opacity: 0; transform: translateY(50px); }
        to { opacity: 1; transform: translateY(0); }
    }

    h1 { 
        font-family: 'Pacifico', cursive;
        font-size: 3.2rem; 
        color: #fff;
        margin: 0 0 15px 0;
        text-shadow: 2px 3px 6px rgba(0,0,0,0.1);
    }

    p { color: #fff; font-size: 1.2rem; font-weight: 500; margin: 8px 0; }

    /* Hugging Bears on Slide 1 */
    .hugging-bears {
        width: 100%;
        max-width: 200px;
        margin: 20px auto;
        display: block;
        animation: gentleShake 4s ease-in-out infinite;
    }

    @keyframes gentleShake {
        0%, 100% { transform: rotate(-3deg); }
        50% { transform: rotate(3deg); }
    }

    /* Keep hands photo on Slide 2 contained and centered only */
    .center-keepsake-img {
        width: 100%;
        max-width: 280px;
        height: auto;
        display: block;
        margin: 25px auto; /* Centers it perfectly vertically and horizontally */
        border: 12px solid #fff;
        border-bottom: 40px solid #fff; /* Polaroid style */
        border-radius: 5px;
        box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        /* Critical for Sharpness Fix: Tells the browser not to smooth it */
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
        transform: scale(1.15); 
        box-shadow: 0 12px 20px rgba(255, 111, 145, 0.4); 
    }

    .no { 
        background: white; 
        color: var(--primary-pink); 
        position: relative; 
        transition: all 0.2s ease;
    }

    /* Second Slide Hidden until Yes is clicked */
    .second-slide {
        display: none;
        animation: fadeIn 1.5s;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }

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
    <div id="slide1">
        <h1>AIMAN ❤️</h1>
        <p>I have a special question for you ✨</p>
        
        <img src="https://i.ibb.co/XzC8fFm/teddy-hug.gif" alt="Hugging Bears" class="hugging-bears">
        
        <p>Will you be mine forever? 💍</p>
        
        <div class="btn-group">
            <button class="yes" onclick="yesClicked()">Yes 😍</button>
            <button class="no" id="no-btn" onmouseover="dodgeButton()" onclick="dodgeButton()">No 😅</button>
        </div>
        
        <p style="font-size:14px; opacity:0.8; margin-top: 30px;">— Yours, Zairuu</p>
    }
    </div>

    <div id="slide2" class="second-slide">
        <h1 style="font-size: 3.5rem;">Yay!!! ❤️</h1>
        <p style="font-size: 1.5rem; margin-top: 20px;">You just made me the happiest person alive, AIMAN! 😍</p>
        
        <img src="https://i.ibb.co/BpDLXMb/1774992960985.png" alt="Our Moment" class="center-keepsake-img">
        
        <p style="margin-top: 15px;">I promise to cherish you every single day.</p>
        <div style="margin-top: 40px; font-family: 'Pacifico'; font-size: 2rem; color: #fff;">Zairuu ❤️</div>
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
    // Switch slides and add a background tint
    document.body.style.background = "linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg')";
    document.body.style.backgroundSize = "cover";
    document.body.style.backgroundPosition = "center";

    // Update Card Appearance for second slide
    document.getElementById('slide1').style.display = 'none';
    document.getElementById('slide2').style.display = 'block';

    // Darken card for text readability against photo
    const card = document.getElementById('main-card');
    card.style.background = "rgba(0, 0, 0, 0.5)";

    // Launch a celebratory heart burst
    for(let i=0; i<30; i++) {
        setTimeout(createHeart, i * 100);
    }
}

function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = ["❤️", "💖", "💝", "💕"][Math.floor(Math.random() * 4)];
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = (Math.random() * 2 + 3) + "s";
    heart.style.fontSize = (Math.random() * 10 + 15) + "px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 5000);
}

// Initial subtle hearts
setInterval(createHeart, 800);
</script>

</body>
</html>
