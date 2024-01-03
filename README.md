# site-de-reservas

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Reservas Online</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background: url('sua-imagem-de-fundo.jpg') no-repeat center center fixed;
      background-size: cover;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    form {
      max-width: 400px;
      background: rgba(255, 255, 255, 0.9);
      padding: 30px;
      border-radius: 8px;
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
    }

    label {
      display: block;
      margin-bottom: 10px;
      font-weight: bold;
    }

    input, select {
      width: 100%;
      padding: 10px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
    }

    button {
      background-color: #4CAF50;
      color: white;
      padding: 15px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 16px;
    }

    button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

  <form id="reservationForm">
    <label for="name">Nome:</label>
    <input type="text" id="name" name="name" required>

    <label for="email">E-mail:</label>
    <input type="email" id="email" name="email" required>

    <label for="date">Data:</label>
    <input type="date" id="date" name="date" required>

    <label for="time">Horário:</label>
    <input type="time" id="time" name="time" required>

    <label for="participants">Número de Participantes:</label>
    <input type="number" id="participants" name="participants" min="1" required>

    <button type="button" onclick="reservar()">Reservar</button>
  </form>

  <script>
    function reservar() {
      var nome = document.getElementById('name').value;
      var email = document.getElementById('email').value;
      var data = document.getElementById('date').value;
      var horario = document.getElementById('time').value;
      var participantes = document.getElementById('participants').value;

      var mensagem = "Olá! Gostaria de fazer uma reserva.%0A%0A";
      mensagem += "Nome: " + nome + "%0A";
      mensagem += "E-mail: " + email + "%0A";
      mensagem += "Data: " + data + "%0A";
      mensagem += "Horário: " + horario + "%0A";
      mensagem += "Número de Participantes: " + participantes;

      window.open("https://wa.me/5564981171364?text=" + encodeURIComponent(mensagem), "_blank");
    }
  </script>

</body>
</html>
