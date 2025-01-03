<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Landing Page - Captura de Leads</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .container {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            text-align: center;
        }

        h1 {
            color: #333;
        }

        p {
            color: #666;
        }

        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            width: 100%;
            padding: 10px;
            background-color: #007BFF;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #0056b3;
        }

        .success-message {
            color: green;
            margin-top: 15px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Entre no Grupo do Telegram</h1>
        <p>Preencha as informações abaixo para entrar no grupo exclusivo.</p>
        <form id="leadForm">
            <input type="text" id="nome" placeholder="Nome Completo" required>
            <input type="email" id="email" placeholder="E-mail" required>
            <input type="tel" id="telefone" placeholder="Telefone" required>
            <button type="submit">Enviar</button>
        </form>
        <p class="success-message" id="successMessage" style="display:none;">
            Obrigado! Você será redirecionado.
        </p>
    </div>

    <script>
        const form = document.getElementById('leadForm');
        const successMessage = document.getElementById('successMessage');

        form.addEventListener('submit', function (e) {
            e.preventDefault();

            const nome = document.getElementById('nome').value;
            const email = document.getElementById('email').value;
            const telefone = document.getElementById('telefone').value;

            if (nome && email && telefone) {
                // Simula o envio do formulário
                console.log('Nome:', nome);
                console.log('E-mail:', email);
                console.log('Telefone:', telefone);

                // Exibe mensagem de sucesso
                successMessage.style.display = 'block';

                // Redireciona para o grupo do Telegram após 2 segundos
                setTimeout(() => {
                    window.location.href = 'https://t.me/tradercabral';
                }, 2000);
            }
        });
    </script>
</body>
</html>
