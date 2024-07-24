<!DOCTYPE html>
<html>
<head>
    <title>Cartinha para a Mãe</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #noButton {
            position: absolute;
        }
    </style>
</head>
<body>
    <h1>Mãe, você me ama?</h1>
    <button onclick="showLove()">Sim</button>
    <button id="noButton" onmouseover="moveNoButton()">Não</button>

    <p id="message"></p>

    <script>
        function showLove() {
            document.getElementById("message").textContent = "Te amo!";
        }

        function moveNoButton() {
            var noButton = document.getElementById("noButton");
            var x = Math.floor(Math.random() * (window.innerWidth - noButton.clientWidth));
            var y = Math.floor(Math.random() * (window.innerHeight - noButton.clientHeight));
            noButton.style.left = x + 'px';
            noButton.style.top = y + 'px';
        }
    </script>
</body>
</html>
