<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Toda minha</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 100px;
            background-image: url('https://media.giphy.com/media/tZYTFIru6T27A1V8xq/giphy.gif'); /* GIF aqui */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            height: 100vh;
            color: white;
        }

        button {
            padding: 10px 20px;
            font-size: 16px;
            margin: 10px;
            cursor: pointer;
            position: relative;
            z-index: 1;
        }

        #nao {
            position: absolute;
        }

        h2, p {
            z-index: 1;
            position: relative;
        }
    </style>
</head>
<body>

    <h2>Quem é minha nenem?</h2>

    <button onclick="responderSim()">Eu</button>
    <button id="nao" onmouseover="fugir()">Não sei</button>

    <p id="resposta"></p>

    <script>
        function responderSim() {
    window.open("https://www.youtube.com/watch?v=YMmDtydK-L0&t=55s", "_blank");

        }

        function fugir() {
            let btn = document.getElementById("nao");
            let largura = window.innerWidth - btn.offsetWidth;
            let altura = window.innerHeight - btn.offsetHeight;

            let novoX = Math.random() * largura;
            let novoY = Math.random() * altura;

            btn.style.left = novoX + "px";
            btn.style.top = novoY + "px";
        }
    </script>

</body>
</html>
