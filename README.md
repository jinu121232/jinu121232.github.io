<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>버튼 폭죽 예시</title>
    <style>
        body {
            background-color: #1e1e1e;
            color: white;
            text-align: center;
            padding: 50px;
            font-family: Arial, sans-serif;
        }
        button {
            background-color: #ff4081;
            color: white;
            padding: 15px 30px;
            font-size: 18px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        button:hover {
            background-color: #ff1f6a;
            transform: scale(1.05);
        }
        #message {
            margin-top: 30px;
            font-size: 24px;
            opacity: 0;
            transition: opacity 1s ease;
        }
    </style>

    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
</head>
<body>

    <h1>이건 버튼이에요</h1>
    <button onclick="celebrate()">버튼</button>

    <div id="message">🎉 축하합니다! 🎉</div>

    <script>
        function celebrate() {

            confetti({
                particleCount: 150,
                spread: 90,
                origin: { y: 0.6 }
            });

            document.getElementById("message").style.opacity = 1;
        }
    </script>

</body>
</html>
