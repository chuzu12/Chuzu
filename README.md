<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Aiman ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@500;700&display=swap" rel="stylesheet">

<style>
    :root {
        --primary-pink: #ff6f91;
        --soft-pink: #ffb6c1;
        --text-color: #555;
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
        font-size: 3.5rem; 
        color: #fff;
        margin: 0 0 15px 0;
        text-shadow: 2px 3px 6px rgba(0,0,0,0.1);
    }

    p { color: #fff; font-size: 1.2rem; font-weight: 500; margin: 8px 0; }

    /* Centered hugging bears on first slide */
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

    .btn-group {
        margin-top: 30px;
        display: flex;
        justify-content: center;
        gap: 20px;
    }

    button {
        padding: 15px 35px;
        border: none;
