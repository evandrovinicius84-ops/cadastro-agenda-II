<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Resultado do Cadastro</title>
</head>
<body>

    <h2>Dados Cadastrados</h2>

    <?php
    if ($_SERVER["REQUEST_METHOD"] == "POST") {
        // Recebendo e armazenando cada informação em sua respectiva variável
        $nome = htmlspecialchars($_POST['nome']);
        $idade = htmlspecialchars($_POST['idade']);
        $profissao = htmlspecialchars($_POST['profissao']);
        $salario = htmlspecialchars($_POST['salario']);
        $experiencia = htmlspecialchars($_POST['experiencia']);

        // Apresentando cada informação em uma linha utilizando elementos HTML
        echo "<p><strong>Nome Completo:</strong> " . $nome . "</p>";
        echo "<p><strong>Idade:</strong> " . $idade . " anos</p>";
        echo "<p><strong>Profissão:</strong> " . $profissao . "</p>";
        echo "<p><strong>Salário Pretendido:</strong> R$ " . $salario . "</p>";
        echo "<p><strong>Experiência Anterior:</strong><br>" . nl2br($experiencia) . "</p>";

        echo "<hr>";

        // Mensagem personalizada utilizando obrigatoriamente o nome, a profissão e a experiência
        echo "<p><strong>Mensagem do Sistema:</strong> Olá, <strong>$nome</strong>! Vimos que você atua como <strong>$profissao</strong> e possui uma trajetória marcada por: <em>\"$experiencia\"</em>. Seu perfil foi analisado com sucesso!</p>";

    } else {
        echo "<p>Nenhum dado foi enviado.</p>";
    }
    ?>

    <br>
    <a href="cadastro.html">Voltar ao Formulário</a>

</body>
</html>
