<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      padding: 0;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #000;
    }

    .page {
      width: 100%;
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;
      transition: transform 0.5s ease;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .page img {
      max-width: 100%;
      max-height: 100%;
      object-fit: cover;
    }

    .chat-widget {
      position: absolute;
      bottom: 10%;
      width: 80%;
      max-width: 400px;
      z-index: 10;
    }

    .hidden {
      transform: translateX(100%);
    }
  </style>
</head>
<body>
  <!-- Prima pagină -->
  <div class="page" id="page1">
    <img src="https://imgcdn.stablediffusionweb.com/2024/9/5/55a97e6e-da03-4b93-b393-43b31121d1d7.jpg" alt="First Image">
    <div class="chat-widget">
      <elevenlabs-convai agent-id="5mz0QGMTS6vciobpmiXO"></elevenlabs-convai>
      <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
    </div>
  </div>

  <!-- A doua pagină -->
  <div class="page hidden" id="page2">
    <img src="https://static.posters.cz/image/1300/postere/spider-man-gotcha-i127936.jpg" alt="Second Image">
    <div class="chat-widget">
      <elevenlabs-convai agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
      <script src="https://elevenlabs.io/convai-widget/index.js" async></script>
    </div>
  </div>

  <script>
    let currentPage = 1;
    document.body.addEventListener('swipe', () => {
      const page1 = document.getElementById('page1');
      const page2 = document.getElementById('page2');

      if (currentPage === 1) {
        page1.classList.add('hidden');
        page2.classList.remove('hidden');
        currentPage = 2;
      } else {
        page1.classList.remove('hidden');
        page2.classList.add('hidden');
        currentPage = 1;
      }
    });
  </script>
</body>
</html>
