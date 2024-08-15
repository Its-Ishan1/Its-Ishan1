<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Romantic Book</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f9f9f9;
            font-family: Arial, sans-serif;
        }
        #book {
            width: 200px;
            height: 300px;
            background-color: #d4a5a5;
            border: 2px solid #a64d4d;
            border-radius: 10px;
            position: relative;
            cursor: pointer;
        }
        #cover {
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            background-color: #d4a5a5;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            font-size: 24px;
            text-align: center;
        }
        #message {
            display: none;
            padding: 20px;
            background-color: #fff;
            border: 2px solid #a64d4d;
            border-radius: 10px;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: #a64d4d;
            font-size: 18px;
            text-align: center;
            z-index: 10;
        }
    </style>
</head>
<body>
    <div id="book">
        <div id="cover">Click Me</div>
        <div id="message"></div>
    </div>
    <script>
        const messages = [
            "🌹 You are my sunshine on a cloudy day! 🌹",
            "💖 Every moment with you is a treasure! 💖",
            "🌟 You make my heart skip a beat! 🌟",
            "💌 I love you more with each passing day! 💌"
        ];

        let currentMessageIndex = 0;
        const book = document.getElementById('book');
        const cover = document.getElementById('cover');
        const messageDiv = document.getElementById('message');

        book.addEventListener('click', () => {
            cover.style.display = 'none';
            messageDiv.style.display = 'block';
            messageDiv.textContent = messages[currentMessageIndex];
            currentMessageIndex = (currentMessageIndex + 1) % messages.length;
        });
    </script>
</body>
</html>

