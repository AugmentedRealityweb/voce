<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #000;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .image-container {
      margin: 10px;
      cursor: pointer;
      transition: transform 0.3s;
    }

    .image-container:hover {
      transform: scale(1.1);
    }

    .image-container img {
      max-width: 300px;
      max-height: 300px;
      object-fit: cover;
      border: 2px solid #fff;
    }
  </style>
</head>
<body>
  <div class="image-container" onclick="openPage('https://augmentedrealityweb.github.io/elsa/')">
    <img src="https://i.pinimg.com/originals/bc/cd/8d/bccd8d514024b3547ef6d05843ce4864.gif" alt="First Image">
  </div>
  <div class="image-container" onclick="openPage('https://augmentedrealityweb.github.io/spiderman/')">
    <img src="https://i.giphy.com/1qErVv5GVUac8uqBJU.webp" alt="Second Image">
  </div>

  <script>
    function openPage(page) {
      window.location.href = page;
    }
  </script>
</body>
</html>
