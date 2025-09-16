<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <title>Marcinek z animowanym tłem</title>
  <style>
    /* Animowane tło na cały ekran */
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      overflow: hidden;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      position: relative;
      color: white;
      text-shadow: 0 0 8px black;
    }

    /* Tło z animowanym GIF-em */
    .background-gif {
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: url('https://i1.kwejk.pl/k/obrazki/2015/02/cf6d88d77f77286a769631f9e98ac849.gif') no-repeat center center;
      background-size: cover;
      z-index: -1;
      filter: brightness(0.7);
    }

    .colorful {
      font-size: 72px;
      font-weight: bold;
      background: linear-gradient(90deg, red, orange, yellow, green, blue, indigo, violet);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: rainbow 3s linear infinite;
    }

    @keyframes rainbow {
      0% {
        background-position: 0%;
      }
      100% {
        background-position: 100%;
      }
    }
  </style>
</head>
<body>
  <div class="background-gif"></div>
  <div class="colorful">Marcinek</div>
</body>
</html>
