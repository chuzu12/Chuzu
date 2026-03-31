# Chuzu
Chuzu proposal
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Chuzu ❤️</title>

<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4);
    height: 100vh;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: #fff;
}

.container {
    background: rgba(0,0,0,0.3);
    padding: 30px;
    border-radius: 20px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    position: relative;
    z-index: 2;
}

h1 {
    font-size: 2.5em;
}

button {
    padding: 12px 25px;
    margin: 10px;
    border: none;
    border-radius: 25px;
    font-size: 16px;
    cursor: pointer;
    transition: 0.3s;
}

.yes {
    background: #28a745;
    color: white;
}

.no {
    background: #dc3545;
    color: white;
}

button:hover {
    transform: scale(1.1);
}

/* hearts */
.heart {
    position: absolute;
    top: -10px;
    color: #ff4d6d;
    font-size: 20px;
    animation: fall linear infinite;
}

@keyframes fall {
    0% {
        transform: translateY(-10px);
        opacity: 1;
    }
    100% {
        transform: translateY(100vh);
        opacity: 0;
    }
}
</style>
</head>

<body>

<div class="container">
    <h1>Chuzu ❤️</h1>
    <p>From the moment I met you, everything felt special ✨</p>
    <p>Will you be mine? 💍</p>
    <p style="font-size:14px; opacity:0.8;">— Zairuu</p>

    <button class="yes" onclick="yesClicked()">Yes 😍</button>
    <button class="no" onmouseover="moveButton()">No 😅</button>
</div>

<script>
function yesClicked() {
    document.body.innerHTML = `
        <div style="text-align:center; color:white;">
            <h1>Yay Chuzu!!! ❤️</h1>
            <p>You just made me the happiest person alive 😍</p>
            <p>Forever yours,</p>
            <h2>Zairuu ❤️</h2>
        </div>
    `;
    createHearts();
}

function moveButton() {
    const button = document.querySelector('.no');
    const x = Math.random() * window.innerWidth;
    const y = Math.random() * window.innerHeight;
    button.style.position = "absolute";
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

        setTimeout(() => {
            heart.remove();
        }, 5000);
    }, 300);
}

// start hearts immediately
createHearts();
</script>

</body>
</html>
