# cadastro-agenda-II
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro de Profissional</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        .container {
            background: #ffffff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 500px;
        }
        h2 {
            margin-bottom: 20px;
            color: #333;
            text-align: center;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
            font-weight: bold;
        }
        input[type="text"],
        input[type="number"],
        textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
            font-size: 14px;
        }
        textarea {
            resize: vertical;
            height: 100px;
        }
        button {
            width: 100%;
            padding: 12px;
            background-color: #007bff;
            border: none;
            border-radius: 4px;
            color: white;
            font-size: 16px;
            cursor: pointer;
            font-weight: bold;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

    <div class="container">
        <h2>Formulário de Cadastro</h2>
        <form action="processaCadastro.php" method="POST">
            
            <div class="form-group">
                <label for="nome">Nome Completo:</label>
                <input type="text" id="nome" name="nome" required>
            </div>

            <div class="form-group">
                <label for="idade">Idade:</label>
                <input type="number" id="idade" name="idade" min="0" required>
            </div>

            <div class="form-group">
                <label for="profissao">Profissão:</label>
                <input type="text" id="profissao" name="profissao" required>
            </div>

            <div class="form-group">
                <label for="salario">Salário Pretendido (R$):</label>
                <input type="text" id="salario" name="salario" placeholder="Ex: 3500.00" required>
            </div>

            <div class="form-group">
                <label for="experiencia">Experiência Anterior:</label>
                <textarea id="experiencia" name="experiencia" placeholder="Descreva brevemente suas experiências anteriores..." required></textarea>
            </div>

            <button type="submit">Cadastrar</button>
            
        </form>
    </div>

</body>
</html>
