<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogo de Clicar</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f7f7f7;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            flex-direction: column;
            text-align: center;
        }
        
        h1 {
            color: #333;
            margin-bottom: 20px;
        }

        #botaoClique {
            background-color: #4CAF50;
            color: white;
            font-size: 24px;
            padding: 20px 40px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
            transition: background-color 0.3s;
        }

        #botaoClique:hover {
            background-color: #45a049;
        }

        #pontuacao {
            font-size: 36px;
            margin-top: 20px;
            color: #333;
        }
    </style>
</head>
<body>

    <h1>Jogo de Clicar</h1>
    <button id="botaoClique">Clique Aqui!</button>
    <div id="pontuacao">Pontos: 0</div>

    <script>
        let pontos = 0;

        // Selecionar os elementos HTML
        const botaoClique = document.getElementById("botaoClique");
        const pontuacao = document.getElementById("pontuacao");

        // Função para atualizar a pontuação
        function atualizarPontuacao() {
            pontos++; // Aumenta 1 ponto a cada clique
            pontuacao.textContent = "Pontos: " + pontos;
        }

        // Adicionar evento de clique no botão
        botaoClique.addEventListener("click", atualizarPontuacao);
    </script>

</body>
</html>
