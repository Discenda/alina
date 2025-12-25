<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Alina ❤️</title>

<style>
    body {
        margin: 0;
        font-family: 'Segoe UI', sans-serif;
        background: linear-gradient(135deg, #ff758c, #ff7eb3);
        color: white;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .box {
        background: rgba(255,255,255,0.15);
        padding: 40px;
        border-radius: 20px;
        max-width: 420px;
        box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        backdrop-filter: blur(10px);
        animation: fadeIn 1.5s ease;
    }

    h1 { font-size: 34px; margin-bottom: 10px; }
    p { font-size: 18px; line-height: 1.6; }
    .heart { font-size: 50px; animation: beat 1.2s infinite; margin: 15px 0; }
    .buttons { margin-top: 25px; position: relative; height: 80px; }
    button { padding: 12px 22px; font-size: 16px; border: none; border-radius: 25px; cursor: pointer; position: absolute; transition: 0.2s; }
    #yes { background: white; color: #ff4f7b; left: 40px; }
    #no { background: rgba(255,255,255,0.4); color: white; right: 40px; }

    @keyframes beat { 0%, 100% { transform: scale(1); } 50% { transform: scale(1.2); } }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
</style>
</head>

<body>
<div class="box">
    <h1>Alina 💖</h1>
    <p>This is not complicated… just one question:</p>
    <div class="heart">❤️</div>
    <p>Do you love me?</p>
    <div class="buttons">
        <button id="yes" onclick="yesClick()">Yes</button>
        <button id="no" onmouseover="moveNo()">No</button>
    </div>
</div>

<script>
function moveNo() {
    const noBtn = document.getElementById("no");
    const x = Math.random() * 250;
    const y = Math.random() * 60;
    noBtn.style.right = "auto";
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}
function yesClick() {
    document.querySelector(".box").innerHTML = `
        <h1>💘 I knew it.</h1>
        <p>Distance doesn’t matter. Neither does time. 😏</p>
        <div class="heart">❤️</div>
        <p>We’ll laugh about this together soon.</p>
    `;
}
</script>

</body>
</html>
