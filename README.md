<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Zalu 💖</title>
<style>
  body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ff758c, #ff7eb3);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Poppins', sans-serif;
    overflow: hidden;
  }
  .card {
    background: white;
    padding: 35px;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 15px 40px rgba(0,0,0,0.25);
    position: relative;
  }
  h1 {
    color: #ff4d6d;
  }
  p {
    font-size: 18px;
    margin-bottom: 25px;
  }
  button {
    padding: 12px 28px;
    font-size: 16px;
    border-radius: 30px;
    border: none;
    cursor: pointer;
    margin: 10px;
  }
  #yes {
    background: #ff4d6d;
    color: white;
  }
  #no {
    background: #ccc;
    position: absolute;
  }
  .heart {
    position: absolute;
    color: red;
    font-size: 20px;
    animation: float 4s infinite;
  }
  @keyframes float {
    0% {transform: translateY(0); opacity: 1;}
    100% {transform: translateY(-800px); opacity: 0;}
  }
</style>
</head>

<body>

<div class="card">
  <h1>Zalu 💕</h1>
  <p>Will you be my Valentine? 🌹</p>
  <button id="yes">Yes 💖</button>
  <button id="no">No 😜</button>
</div>

<script>
const noBtn = document.getElementById("no");
const yesBtn = document.getElementById("yes");

noBtn.addEventListener("mouseover", () => {
  const x = Math.random() * (window.innerWidth - 120);
  const y = Math.random() * (window.innerHeight - 60);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
});

yesBtn.addEventListener("click", () => {
  document.body.innerHTML = `
    <div style="text-align:center;color:white;">
      <h1>Yayyy Zalu 💖😍</h1>
      <h2>You just made my day 🌹</h2>
      <p>This Valentine is officially special 💫</p>
    </div>
  `;
  for(let i=0;i<40;i++){
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random()*100 + "vw";
    heart.style.bottom = "0px";
    heart.style.animationDuration = (2 + Math.random()*3) + "s";
    document.body.appendChild(heart);
  }
});
</script>

</body>
</html>
