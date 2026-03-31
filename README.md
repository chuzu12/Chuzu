<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Aiman ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">

<style>
    body {
        margin: 0;
        font-family: 'Pacifico', cursive;
        background: url('https://i.ibb.co/3fM7Vx6/teddy-bg.jpg') no-repeat center center fixed;
        background-size: cover;
        height: 100vh;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: #fff;
        transition: background 1s ease-in-out;
    }

    .container {
        background: rgba(255, 192, 203, 0.6); 
        padding: 30px;
        border-radius: 30px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.3);
        position: relative;
        z-index: 2;
        max-width: 400px;
        width: 90%;
        backdrop-filter: blur(2px);
    }

    h1 { font-size: 2.8em; margin-bottom: 10px; text-shadow: 2px 2px 4px rgba(0,0,0,0.2); }

    /* Image Styling: Sharp and Centered on Second Page */
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

    button {
        padding: 12px 25px;
        margin: 10px;
        border: none;
        border-radius: 50px;
        font-size: 18px;
        cursor: pointer;
        transition: 0.3s;
        font-family: 'Pacifico', cursive;
        box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }

    .yes { background: #ff6f91; color: white; }
    .no { background: #ffb6c1; color: white; position: relative; transition: all 0.2s ease; }

    button:hover { transform: scale(1.1); }

    /* Hearts */
    .heart {
        position: absolute;
        top: -10px;
        color: #ff4d6d;
        font-size: 25px;
        animation: fall linear infinite;
        z-index: 1;
    }

    @keyframes fall {
        0% { transform: translateY(-10px); opacity: 1; }
        100% { transform: translateY(100vh); opacity: 0; }
    }
</style>
</head>

<body>

<div class="container" id="main-card">
    <h1>Aiman ❤️</h1>
    <p>From the moment I met you, everything felt special ✨</p>
    
    <p>Will you be mine? 💍</p>
    <p style="font-size:14px; opacity:0.8; margin-top: 10px;">— Your Zairuu</p>

    <button class="yes" onclick="yesClicked()">Yes 😍</button>
    <button class="no" onmouseover="moveButton()">No 😅</button>
</div>

<script>
function yesClicked() {
    // Reveal original photo as full background
    document.body.style.background = "linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('https://instasize.com/p/2d6cfc6ee3a44864ce0e8b6405149163bf54a712c2857e7e72250e49f4662393')";
    document.body.style.backgroundSize = "cover";
    document.body.style.backgroundPosition = "center";

    const card = document.getElementById('main-card');
    card.style.background = "rgba(0, 0, 0, 0.5)";
    card.innerHTML = `
        <h1 style="font-size: 3em;">Yay Aiman!!! ❤️</h1>
        <p style="font-size: 1.3em;">You just made me the happiest person alive 😍</p>
        
        <img src="https://instasize.com/p/2d6cfc6ee3a44864ce0e8b6405149163bf54a712c2857e7e72250e49f4662393" alt="Our Moment" class="center-keepsake-img">
        
        <p>I can't wait for our forever.</p>
        <br>
        <h2 style="font-size: 2em; margin: 0;">Zairuu ❤️</h2>
    `;

    createHearts();
}

function moveButton() {
    const button = document.querySelector('.no');
    const x = Math.random() * (window.innerWidth - button.offsetWidth);
    const y = Math.random() * (window.innerHeight - button.offsetHeight);
    button.style.position = "fixed";
    button.style.left = x + "px";
    button.style.top = y + "px";
}

function createHearts() {
    setInterval(() => {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "❤";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
        document.body.appendChild(heart);
        setTimeout(() => { heart.remove(); }, 5000);
    }, 300);
}

createHearts();
</script>

</body>
</html>
