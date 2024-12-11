<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Payment Integration</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #f0f0f0;
      margin: 0;
      padding: 20px;
    }

    #content {
      display: none;
      margin-top: 20px;
    }

    .payment-option {
      margin: 10px 0;
    }
  </style>
</head>
<body>
  <h1>Welcome to the App</h1>
  <p id="timer">You have 10 seconds of free usage!</p>
  <div id="content">
    <h2>Enjoy the app!</h2>
    <p>Interactive content goes here.</p>
  </div>
  <div id="payment" style="display: none;">
    <h2>Time Expired</h2>
    <p>Please purchase more time to continue:</p>
    <div class="payment-option">
      <a href="https://revolut.me/r/9ouIF7WVBU" target="_blank">10 minutes - 15 RON</a>
    </div>
    <div class="payment-option">
      <a href="https://revolut.me/r/qTzpX33NT1" target="_blank">30 minutes - 25 RON</a>
    </div>
    <div class="payment-option">
      <a href="https://revolut.me/r/Z0QtuDZnEQ" target="_blank">60 minutes - 50 RON</a>
    </div>
  </div>
  <script>
    let timer = 10;
    const timerElement = document.getElementById("timer");
    const contentElement = document.getElementById("content");
    const paymentElement = document.getElementById("payment");

    const interval = setInterval(() => {
      timer -= 1;
      timerElement.textContent = `You have ${timer} seconds of free usage!`;
      if (timer <= 0) {
        clearInterval(interval);
        timerElement.style.display = "none";
        contentElement.style.display = "none";
        paymentElement.style.display = "block";
      }
    }, 1000);

    // Simulate access extension after payment manually
    // Example: set contentElement.style.display = "block" and paymentElement.style.display = "none" after verifying payment
  </script>
</body>
</html>
