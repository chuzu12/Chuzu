<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Chuzu ❤️</title>

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
        transition: background 1s ease-in-out; /* Smooth background fade */
    }

    .container {
        background: rgba(255, 192, 203, 0.5); /* soft pink overlay */
        padding: 30px;
        border-radius: 30px;
        box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        position: relative;
        z-index: 2;
        max-width: 85%;
        backdrop-filter: blur(5px); /* Adds a modern glassy feel */
    }

    h1 { font-size: 3em; margin-bottom: 10px; }

    button {
        padding: 15px 30px;
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

    /* The Success State Styling */
    .success-container {
        background: rgba(0, 0, 0, 0.4); /* Darker overlay to make text pop against your photo */
        padding: 40px;
        border-radius: 30px;
        animation: fadeIn 1.5s;
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }

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
    <h1>Chuzu ❤️</h1>
    <p>From the moment I met you, everything felt special ✨</p>
    <p>Will you be mine? 💍</p>
    <p style="font-size:16px; opacity:0.9;">— Zairuu</p>

    <button class="yes" onclick="yesClicked()">Yes 😍</button>
    <button class="no" onmouseover="moveButton()">No 😅</button>
</div>

<script>
function yesClicked() {
    // 1. Change the background to your specific photo
    document.body.style.background = "url('https://i.ibb.co/yFh64j3c/1000106114.jpg') no-repeat center center fixed";
    document.body.style.backgroundSize = "cover";

    // 2. Update the content with a clearer overlay
    const card = document.getElementById('main-card');
    card.className = "success-container";
    card.innerHTML = `
        <h1 style="font-size: 3.5em;">Yay Chuzu!!! ❤️</h1>
        <p style="font-size: 1.5em;">You just made me the happiest person alive 😍</p>
        <p>I promise to hold your hand forever.</p>
        <br>
        <p>Forever yours,</p>
        <h2 style="font-size: 2.5em; margin: 0;">Zairuu ❤️</h2>
    `;

    createHearts();
}

// Makes the No button dodge
function moveButton() {
    const button = document.querySelector('.no');
    const x = Math.random() * (window.innerWidth - button.offsetWidth);
    const y = Math.random() * (window.innerHeight - button.offsetHeight);
    button.style.position = "fixed";
    button.style.left = x + "px";
    button.style.top = y + "px";
}

// Falling hearts animation
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
