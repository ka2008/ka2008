<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="styles.css">
  <title>Snake Game</title>
</head>
<body>
  <div id="snake"></div>
  <script src="script.js"></script>
</body>
</html>

#snake {
  width: 20px;
  height: 20px;
  background-color: green;
  position: absolute;
}

document.addEventListener('DOMContentLoaded', function () {
  const snake = document.getElementById('snake');

  function moveSnake() {
    const left = Math.floor(Math.random() * window.innerWidth);
    const top = Math.floor(Math.random() * window.innerHeight);

    snake.style.left = left + 'px';
    snake.style.top = top + 'px';
  }

  setInterval(moveSnake, 1000); // Move a cobrinha a cada segundo
});
