<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NÚMEROS PARA MEGA SENA</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        .numeros {
            font-size: 24px;
            font-weight: bold;
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Sorteio de 6 Números</h1>
    <button onclick="sortearNumeros()">Sortear</button>
    <div class="numeros" id="resultado"></div>
    
    <script>
        function sortearNumeros() {
            let numeros = new Set();
            while (numeros.size < 6) {
                let numero = Math.floor(Math.random() * 60) + 1;
                numeros.add(numero);
            }
            document.getElementById("resultado").textContent = Array.from(numeros).sort((a, b) => a - b).join(" - ");
        }
    </script>
</body>
</html>
