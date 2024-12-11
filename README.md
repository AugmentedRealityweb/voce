<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paywall</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
        }

        #paywall {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            padding: 20px;
        }

        .paywall-content {
            background-color: #333;
            border-radius: 10px;
            padding: 20px;
            max-width: 400px;
            margin: 50px auto;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <h1>Welcome to the conversation!</h1>
    <p>Enjoy your time here. A paywall will appear shortly...</p>

    <div id="paywall">
        <div class="paywall-content">
            <h2>Purchase More Conversation Time</h2>
            <p>Select your desired time extension:</p>
            <ul>
                <li>10 minutes: 15 lei - <a href="https://revolut.me/r/9ouIF7WVBU" target="_blank">Pay Now</a></li>
                <li>30 minutes: 25 lei - <a href="https://revolut.me/r/qTzpX33NT1" target="_blank">Pay Now</a></li>
                <li>60 minutes: 50 lei - <a href="https://revolut.me/r/Z0QtuDZnEQ" target="_blank">Pay Now</a></li>
            </ul>
            <p>After payment, enter the code received on Revolut to unlock access:</p>
            <input type="text" id="code-input" placeholder="Enter your code">
            <button onclick="validateCode()">Unlock</button>
            <p id="error-message" class="hidden">Invalid code. Please try again.</p>
        </div>
    </div>

    <script>
        const validCodes = {
            "1234": 10,
            "2345": 30,
            "3456": 60
        };

        let countdown;

        function showPaywall() {
            document.getElementById('paywall').style.display = 'block';
        }

        function hidePaywall() {
            document.getElementById('paywall').style.display = 'none';
        }

        function validateCode() {
            const code = document.getElementById('code-input').value;
            const errorMessage = document.getElementById('error-message');
            
            if (validCodes[code]) {
                errorMessage.classList.add('hidden');
                hidePaywall();
                startTimer(validCodes[code]);
            } else {
                errorMessage.classList.remove('hidden');
            }
        }

        function startTimer(minutes) {
            const endTime = Date.now() + minutes * 60000;

            if (countdown) clearInterval(countdown);

            countdown = setInterval(() => {
                const timeLeft = endTime - Date.now();

                if (timeLeft <= 0) {
                    clearInterval(countdown);
                    showPaywall();
                }
            }, 1000);
        }

        setTimeout(showPaywall, 10000); // Show paywall after 10 seconds
    </script>
</body>
</html>
