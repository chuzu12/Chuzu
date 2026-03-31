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
        --glass-bg: rgba(255, 255, 255, 0.3);
    }

    body {
        margin: 0;
        padding: 0;
        font-family: 'Quicksand', sans-serif;
        background: url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg') no-repeat center center fixed;
        background-size: cover;
        height: 100vh;
        width: 100vw;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        transition: background 1.2s ease-in-out;
    }

    .container {
        background: var(--glass-bg);
        backdrop-filter: blur(15px);
        -webkit-backdrop-filter: blur(15px);
        border: 1px solid rgba(255, 255, 255, 0.4);
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

    /* Centered Image Styling */
    .center-img {
        width: 100%;
        max-width: 250px;
        height: auto;
        display: block;
        margin: 20px auto;
        border: 10px solid #fff;
        border-bottom: 40px solid #fff; /* Polaroid style */
        border-radius: 4px;
        box-shadow: 0 12px 25px rgba(0,0,0,0.2);
        image-rendering: -webkit-optimize-contrast;
        object-fit: contain;
        transform: rotate(-2deg); /* Added a slight cute tilt */
    }

    .btn-group {
        margin-top: 30px;
        display: flex;
        justify-content: center;
        gap: 20px;
        min-height: 70px; /* Space for the button to live */
    }

    button {
        padding: 15px 30px;
        border: none;
        border-radius: 50px;
        font-size: 1.1rem;
        font-weight: 700;
        cursor: pointer;
        font-family: 'Quicksand', sans-serif;
        box-shadow: 0 8px 15px rgba(0,0,0,0.1);
    }

    .yes { 
        background: var(--primary-pink); 
        color: white; 
        transition: transform 0.3s ease;
    }
    .yes:hover { transform: scale(1.1); }

    .no { 
        background: #fff; 
        color: var(--primary-pink); 
        position: relative; /* Starts relative, becomes fixed on first move */
        transition: all 0.3s cubic-bezier(0.19, 1, 0.22, 1);
        white-space: nowrap;
    }

    /* Second Slide Style */
    #slide2 { display: none; }
    
    .fade-in {
        animation: fadeIn 1.2s forwards;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: scale(0.9); }
        to { opacity: 1; transform: scale(1); }
    }

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
        <p>You make my world a better place... ✨</p>
        
        <img src="https://i.ibb.co/yFh64j3c/1000106114.jpg" alt="Our Photo" class="center-img">
        
        <p>Will you be mine forever? 💍</p>
        
        <div class="btn-group">
            <button class="yes" onclick="yesClicked()">Yes 😍</button>
            <button class="no" id="no-btn" onmouseover="dodgeButton()" onclick="dodgeButton()">No 😅</button>
        </div>
        <p style="font-size:14px; opacity:0.9; margin-top: 25px;">— Yours, Zairuu</p>
    </div>

    <div id="slide2" class="fade-in">
        <h1 style="font-size: 3.5rem;">YAY!!! ❤️</h1>
        <p style="font-size: 1.4rem; margin: 15px 0;">You've made me the happiest person alive, AIMAN! 😍</p>
        
        <img src="https://i.ibb.co/yFh64j3c/1000106114.jpg" alt="Our Forever" class="center-img" style="transform: rotate(2deg);">
        
        <p>I can't wait to spend forever with you.</p>
        <div style="margin-top: 35px; font-family: 'Pacifico'; font-size: 2.2rem; color: #fff;">Zairuu ❤️</div>
    </div>
</div>

<script>
const quotes = ["Are you sure? 🤨", "Nice try! 😉", "Wrong button! ❌", "Try again! ✨", "Not today! 🏃‍♀️", "Catch me! 💨"];

function dodgeButton() {
    const btn = document.getElementById('no-btn');
    
    // Change text randomly
    btn.innerHTML = quotes[Math.floor(Math.random() * quotes.length)];
    
    // Calculate boundaries to keep button visible on screen
    const padding = 50;
    const maxX = window.innerWidth - btn.offsetWidth - padding;
    const maxY = window.innerHeight - btn.offsetHeight - padding;
    
    const randomX = Math.max(padding, Math.floor(Math.random() * maxX));
    const randomY = Math.max(padding, Math.floor(Math.random() * maxY));
    
    // Set fixed position and move it
    btn.style.position = "fixed";
    btn.style.left = randomX + "px";
    btn.style.top = randomY + "px";
}

function yesClicked() {
    // 1. Darken background and keep image
    document.body.style.background = "linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg')";
    document.body.style.backgroundSize = "cover";
    
    // 2. Switch Slides
    document.getElementById('slide1').style.display = 'none';
    document.getElementById('slide2').style.display = 'block';
    
    // 3. Update Card Appearance
    document.getElementById('main-card').style.background = "rgba(0, 0, 0, 0.6)";
    
    // 4. Celebration Burst
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
    setTimeout(() => heart.remove(), 5000);
}

// Subtle ambient hearts
setInterval(createHeart, 1000);
</script>

</body>
</html>
