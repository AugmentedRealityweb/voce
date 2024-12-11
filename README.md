<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    body {
      margin: 0;
      padding: 0;
      overflow: hidden; 
    }

    .chat-widget {
      width: 50%;
      position: absolute;
      top: 0;
      bottom: 0;
      overflow: hidden;
    }

    /* Primul widget - stânga */
    .chat-widget:first-of-type {
      left: 0;
    }

    /* Al doilea widget - dreapta */
    .chat-widget:last-of-type {
      right: 0;
    }

    #paywall {
      display: none; 
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.8);
      z-index: 9999;
      text-align: center;
      color: white;
      font-family: Arial, sans-serif;
    }

    #paywall-content {
      position: relative;
      top: 50%;
      transform: translateY(-50%);
    }

    #paywall-content h1 {
      margin-bottom: 20px;
      font-size: 2em;
    }

    #paywall-content a {
      color: #fff;
      font-size: 1.5em;
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <!-- Agent stânga -->
  <div class="chat-widget">
    <div class="chat-widget-body">
      <!-- Widget content stânga -->
      <elevenlabs-convai agent-id="5mz0QGMTS6vciobpmiXO"></elevenlabs-convai>
      <script src="https://elevenlabs.io/convai-widget/index.js" async type="text/javascript"></script>
    </div>
  </div>

  <!-- Agent dreapta -->
  <div class="chat-widget">
    <div class="chat-widget-body">
      <!-- Widget content dreapta -->
      <elevenlabs-convai agent-id="sNEfrsQUklzPW2Hu6VGg"></elevenlabs-convai>
      <script src="https://elevenlabs.io/convai-widget/index.js" async type="text/javascript"></script>
    </div>
  </div>

  <!-- Paywall overlay -->
  <div id="paywall">
    <div id="paywall-content">
      <h1>Accesul la conținut este limitat</h1>
      <p>Pentru a continua vizionarea, te rugăm să efectuezi plata:</p>
      <a href="https://revolut.me/r/oXoYVOfoyM" target="_blank">Click aici pentru plată</a>
    </div>
  </div>

  <script>
    // Afișează paywall-ul după 20 de secunde
    setTimeout(function() {
      document.getElementById('paywall').style.display = 'block';
    }, 20000);
  </script>
</body>
</html>
