<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body, html {
      height: 100%;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(45deg, #ff4500, #ff6347, #ff8c00, #ffd700);
      background-size: 400% 400%;
      animation: lava-animation 5s ease infinite;
    }

    @keyframes lava-animation {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .chat-widget {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 400px;
      height: 500px;
      background-color: rgba(255, 255, 255, 0.9);
      border-radius: 20px;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
      display: flex;
      flex-direction: column;
    }

    .chat-widget-header {
      background-color: #a1887f;
      color: white;
      padding: 20px;
      text-align: center;
      font-size: 20px;
      font-weight: bold;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }

    .chat-widget-body {
      flex: 1;
      padding: 20px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      background-color: #f4f4f4;
      border-radius: 15px;
    }

    elevenlabs-convai {
      width: 100%;
      height: 100%;
    }

    .ar-button {
      background-color: #ff6347;
      color: white;
      border: none;
      padding: 12px 20px;
      border-radius: 20px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .ar-button:hover {
      background-color: #ff4500;
    }
  </style>
  <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
</head>
<body>

  <div class="chat-widget">
    <div class="chat-widget-header">Chat with Us</div>
    <div class="chat-widget-body" id="chat-widget-body">
      <elevenlabs-convai agent-id="5mz0QGMTS6vciobpmiXO"></elevenlabs-convai>
      <script src="https://elevenlabs.io/convai-widget/index.js" async type="text/javascript"></script>
    </div>
  </div>

</body>
</html>
