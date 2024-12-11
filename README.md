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
    <img src="https://imgcdn.stablediffusionweb.com/2024/9/5/55a97e6e-da03-4b93-b393-43b31121d1d7.jpg" alt="First Image">
  </div>
  <div class="image-container" onclick="openPage('https://augmentedrealityweb.github.io/spiderman/')">
    <img src="https://static.posters.cz/image/1300/postere/spider-man-gotcha-i127936.jpg" alt="Second Image">
  </div>

  <script>
    function openPage(page) {
      window.location.href = page;
    }
  </script>
</body>
</html>
