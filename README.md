# potential-octo-adventure
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Valentine ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Arial, sans-serif;
      background: linear-gradient(135deg, #ff4b5c, #ff9a9e);
      color: white;
      text-align: center;
      overflow-x: hidden;
    }header {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  animation: fadeIn 2s ease-in-out;
}

h1 {
  font-size: 3em;
  margin-bottom: 10px;
}

p {
  font-size: 1.3em;
  max-width: 600px;
}

button {
  margin-top: 20px;
  padding: 12px 25px;
  font-size: 18px;
  border: none;
  border-radius: 25px;
  background: white;
  color: #ff4b5c;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  transform: scale(1.1);
  background: #ffe3e6;
}

section {
  padding: 60px 20px;
  background: rgba(0,0,0,0.15);
  margin: 20px;
  border-radius: 20px;
}

.heart {
  position: fixed;
  top: -10px;
  color: red;
  animation: fall linear forwards;
}

@keyframes fall {
  to {
    transform: translateY(110vh);
  }
}

@keyframes fadeIn {
  from {opacity: 0; transform: translateY(20px);} 
  to {opacity: 1; transform: translateY(0);} 
}

footer {
  padding: 20px;
  font-size: 14px;
  opacity: 0.8;
}

  </style>
</head>
<body><header>
  <h1>Happy Valentine's Day ❤️</h1>
  <p>To the most beautiful girl in my life, this small website is made just for you.</p>
  <a href="message.html" style="text-decoration:none;">
    <button>Click me 💌</button>
  </a>
</header><section id="message" style="display:none;">
  <h2>My Love Letter</h2>
  <p>
    From the moment I met you, my life became brighter. Your smile, your voice, and everything about you makes me happy.
    <br><br>
    Thank you for being part of my life. I promise to love you, care for you, and make you smile every day.
    <br><br>
    I love you forever ❤️
  </p>
</section><section>
  <h2>Why I Love You 💖</h2>
  <p>
    • Your beautiful smile 😊<br>
    • Your kindness 💕<br>
    • You make me feel special ✨<br>
    • You are my everything ❤️
  </p>
</section><section>
  <h2>Our Forever Countdown ⏳</h2>
  <p id="countdown"></p>
</section><footer>
  Made with ❤️ by Your Boyfriend
</footer><script>
  function showMessage() {
    document.getElementById('message').style.display = 'block';
  }

  // Floating hearts
  function createHeart() {
    const heart = document.createElement('div');
    heart.classList.add('heart');
    heart.innerHTML = '❤️';
    heart.style.left = Math.random() * window.innerWidth + 'px';
    heart.style.fontSize = (Math.random() * 20 + 10) + 'px';
    heart.style.animationDuration = (Math.random() * 3 + 2) + 's';
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 5000);
  }

  setInterval(createHeart, 300);

  // Countdown example (change date if needed)
  const targetDate = new Date("Feb 14, 2027 00:00:00").getTime();

  const countdown = setInterval(function() {
    const now = new Date().getTime();
    const distance = targetDate - now;

    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((distance % (1000 * 60)) / 1000);

    document.getElementById("countdown").innerHTML =
      days + " days " + hours + " hours " + minutes + " minutes " + seconds + " seconds";

    if (distance < 0) {
      clearInterval(countdown);
      document.getElementById("countdown").innerHTML = "Forever with you ❤️";
    }
  }, 1000);
</script></body>
</html>
