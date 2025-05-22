## 👋 Olá! Seja bem-vindo ao meu GitHub

Sou um desenvolvedor apaixonado por tecnologia, código limpo e... café quente!

### ⚙️ Sistema de produtividade:

☑️ Código limpo  
☑️ Café na caneca  
☕ **Status:** Refill em andamento...

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Xícara de Café</title>
  <style>
    body {
      background: #f8f3f0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
    }

    .cup {
      position: relative;
      width: 100px;
      height: 120px;
      background: #fff;
      border-radius: 0 0 50px 50px;
      border: 4px solid #333;
      overflow: hidden;
    }

    .coffee {
      position: absolute;
      bottom: 0;
      width: 100%;
      height: 0%;
      background: #6f4e37;
      transition: height 1s ease-in-out;
      border-radius: 0 0 40px 40px;
    }

    .handle {
      position: absolute;
      right: -30px;
      top: 30px;
      width: 40px;
      height: 60px;
      border: 4px solid #333;
      border-left: none;
      border-radius: 0 50% 50% 0;
    }

    button {
      margin-top: 20px;
      padding: 10px 20px;
      border: none;
      background: #6f4e37;
      color: #fff;
      font-weight: bold;
      cursor: pointer;
      border-radius: 8px;
      box-shadow: 0 4px #444;
    }

    button:hover {
      background: #5b3e2c;
    }
  </style>
</head>
<body>
  <div class="cup">
    <div class="coffee" id="coffee"></div>
    <div class="handle"></div>
  </div>
  <button onclick="refillCoffee()">☕ Refill!</button>

  <script>
    function refillCoffee() {
      const coffee = document.getElementById('coffee');
      coffee.style.height = '100%';
      setTimeout(() => {
        coffee.style.height = '0%';
      }, 3000);
    }
  </script>
</body>
</html>
