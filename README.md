
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de IMC</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 50px;
        }
        .container {
            max-width: 300px;
            margin: auto;
        }
        input, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Calculadora de IMC</h2>
        <input type="number" id="peso" placeholder="Peso (kg)" step="0.1">
        <input type="number" id="altura" placeholder="Altura (m)" step="0.01">
        <button onclick="calcularIMC()">Calcular IMC</button>
        <p id="resultado"></p>
    </div>

    <script>
        function calcularIMC() {
            // Captura os valores de peso e altura
            const peso = parseFloat(document.getElementById('peso').value);
            const altura = parseFloat(document.getElementById('altura').value);

            // Calcula o IMC
            const imc = peso / (altura * altura);

            // Exibe o resultado
            let resultado = `Seu IMC é ${imc.toFixed(2)}. `;
            if (imc < 18.5) {
                resultado += "Você está abaixo do peso.";
            } else if (imc >= 18.5 && imc < 25) {
                resultado += "Você está com peso normal.";
            } else if (imc >= 25 && imc < 30) {
                resultado += "Você está com sobrepeso.";
            } else {
                resultado += "Você está obeso.";
            }

            document.getElementById('resultado').innerText = resultado;
        }
    </script>
</body>
</html>
