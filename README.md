<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Download Script</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 100px;
    }
    .btn {
      background-color: #2d72d9;
      color: white;
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }
    .btn:hover {
      background-color: #1a4fa3;
    }
  </style>
</head>
<body>
  <h1>Baixar Script</h1>
  <p>Clique no botão abaixo para baixar o script:</p>
  <a href="https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/main/script.lua" download>
    <button class="btn">⬇️ Download Script</button>
  </a>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
      background: #f3f4f6;
    }
    .login-box {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
    }
    input {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 80%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    button {
      background: #2d72d9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    button:hover {
      background: #1a4fa3;
    }
  </style>
</head>
<body>
  <div class="login-box">
    <h2>Login</h2>
    <input type="text" id="user" placeholder="Usuário">
    <input type="password" id="pass" placeholder="Senha">
    <button onclick="login()">Entrar</button>
    <p id="msg" style="color:red;"></p>
  </div>

  <script>
    function login() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      // 🔒 Usuário e senha fixos (altere aqui)
      const USERNAME = "admin";
      const PASSWORD = "12345";

      if (user === USERNAME && pass === PASSWORD) {
        window.location.href = "index.html"; // página liberada
      } else {
        document.getElementById("msg").innerText = "Usuário ou senha incorretos!";
      }
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login + Menu</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f4f6;
    }

    /* Tela de login */
    #login-box {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 300px;
      width: 100%;
    }

    .login-card input {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 90%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .login-card button {
      background: #2d72d9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-card button:hover {
      background: #1a4fa3;
    }

    /* Barra do menu */
    nav {
      width: 100%;
      padding: 15px 0;
      text-align: center;
      background: linear-gradient(270deg, #ff6b6b, #f7d794, #1dd1a1, #54a0ff, #5f27cd);
      background-size: 1000% 1000%;
      animation: gradientShift 12s ease infinite;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 20px;
      font-size: 18px;
      font-weight: bold;
      transition: 0.3s;
    }

    nav a:hover {
      text-decoration: underline;
      font-size: 20px;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Conteúdo */
    #conteudo {
      display: none;
    }

    section {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 32px;
    }
  </style>
</head>
<body>
  <!-- Tela de Login -->
  <div id="login-box">
    <div class="login-card">
      <h2>Login</h2>
      <input type="text" id="user" placeholder="Usuário">
      <input type="password" id="pass" placeholder="Senha">
      <button onclick="login()">Entrar</button>
      <p id="msg" style="color:red;"></p>
    </div>
  </div>

  <!-- Conteúdo com Menu -->
  <div id="conteudo">
    <nav>
      <a href="#home">🏠 Início</a>
      <a href="#sobre">ℹ️ Sobre</a>
      <a href="#scripts">💻 Scripts</a>
      <a href="#contato">📩 Contato</a>
    </nav>

    <section id="home">Bem-vindo ao meu site 🚀</section>
    <section id="sobre">Sobre mim ✨</section>
    <section id="scripts">Scripts disponíveis ⚡</section>
    <section id="contato">Entre em contato 📱</section>
  </div>

  <script>
    function login() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      // 🔒 Usuário e senha fixos (troque aqui)
      const USERNAME = "admin";
      const PASSWORD = "12345";

      if (user === USERNAME && pass === PASSWORD) {
        document.getElementById("login-box").style.display = "none";
        document.getElementById("conteudo").style.display = "block";
      } else {
        document.getElementById("msg").innerText = "Usuário ou senha incorretos!";
      }
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login + Menu</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f4f6;
    }

    /* Tela de login */
    #login-box {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 300px;
      width: 100%;
    }

    .login-card input {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 90%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .login-card button {
      background: #2d72d9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-card button:hover {
      background: #1a4fa3;
    }

    /* Barra do menu */
    nav {
      width: 100%;
      padding: 15px 0;
      text-align: center;
      background: linear-gradient(270deg, #ff6b6b, #f7d794, #1dd1a1, #54a0ff, #5f27cd);
      background-size: 1000% 1000%;
      animation: gradientShift 12s ease infinite;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 20px;
      font-size: 18px;
      font-weight: bold;
      transition: 0.3s;
    }

    nav a:hover {
      text-decoration: underline;
      font-size: 20px;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Conteúdo */
    #conteudo {
      display: none;
    }

    section {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 32px;
    }
  </style>
</head>
<body>
  <!-- Tela de Login -->
  <div id="login-box">
    <div class="login-card">
      <h2>Login</h2>
      <input type="text" id="user" placeholder="Usuário">
      <input type="password" id="pass" placeholder="Senha">
      <button onclick="login()">Entrar</button>
      <p id="msg" style="color:red;"></p>
    </div>
  </div>

  <!-- Conteúdo com Menu -->
  <div id="conteudo">
    <nav>
      <a href="#home">🏠 Início</a>
      <a href="#sobre">ℹ️ Sobre</a>
      <a href="#scripts">💻 Scripts</a>
      <a href="#contato">📩 Contato</a>
    </nav>

    <section id="home">Bem-vindo ao meu site 🚀</section>
    <section id="sobre">Sobre mim ✨</section>
    <section id="scripts">Scripts disponíveis ⚡</section>
    <section id="contato">Entre em contato 📱</section>
  </div>

  <script>
    function login() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      // 🔒 Usuário e senha fixos (troque aqui)
      const USERNAME = "admin";
      const PASSWORD = "12345";

      if (user === USERNAME && pass === PASSWORD) {
        document.getElementById("login-box").style.display = "none";
        document.getElementById("conteudo").style.display = "block";
      } else {
        document.getElementById("msg").innerText = "Usuário ou senha incorretos!";
      }
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login + Menu</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f4f6;
    }

    /* Tela de login */
    #login-box {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 300px;
      width: 100%;
    }

    .login-card input {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 90%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .login-card button {
      background: #2d72d9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-card button:hover {
      background: #1a4fa3;
    }

    /* Barra do menu */
    nav {
      width: 100%;
      padding: 15px 0;
      text-align: center;
      background: linear-gradient(270deg, #ff6b6b, #f7d794, #1dd1a1, #54a0ff, #5f27cd);
      background-size: 1000% 1000%;
      animation: gradientShift 12s ease infinite;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 20px;
      font-size: 18px;
      font-weight: bold;
      transition: 0.3s;
    }

    nav a:hover {
      text-decoration: underline;
      font-size: 20px;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Conteúdo */
    #conteudo {
      display: none;
    }

    section {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 32px;
    }
  </style>
</head>
<body>
  <!-- Tela de Login -->
  <div id="login-box">
    <div class="login-card">
      <h2>Login</h2>
      <input type="text" id="user" placeholder="Usuário">
      <input type="password" id="pass" placeholder="Senha">
      <button onclick="login()">Entrar</button>
      <p id="msg" style="color:red;"></p>
    </div>
  </div>

  <!-- Conteúdo com Menu -->
  <div id="conteudo">
    <nav>
      <a href="#home">🏠 Início</a>
      <a href="#sobre">ℹ️ Sobre</a>
      <a href="#scripts">💻 Scripts</a>
      <a href="#contato">📩 Contato</a>
    </nav>

    <section id="home">Bem-vindo ao meu site 🚀</section>
    <section id="sobre">Sobre mim ✨</section>
    <section id="scripts">Scripts disponíveis ⚡</section>
    <section id="contato">Entre em contato 📱</section>
  </div>

  <script>
    function login() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      // 🔒 Usuário e senha fixos (troque aqui)
      const USERNAME = "admin";
      const PASSWORD = "12345";

      if (user === USERNAME && pass === PASSWORD) {
        document.getElementById("login-box").style.display = "none";
        document.getElementById("conteudo").style.display = "block";
      } else {
        document.getElementById("msg").innerText = "Usuário ou senha incorretos!";
      }
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login + Menu</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f4f6;
    }

    /* Tela de login */
    #login-box {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 300px;
      width: 100%;
    }

    .login-card input {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 90%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .login-card button {
      background: #2d72d9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-card button:hover {
      background: #1a4fa3;
    }

    /* Barra do menu */
    nav {
      width: 100%;
      padding: 15px 0;
      text-align: center;
      background: linear-gradient(270deg, #ff6b6b, #f7d794, #1dd1a1, #54a0ff, #5f27cd);
      background-size: 1000% 1000%;
      animation: gradientShift 12s ease infinite;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 20px;
      font-size: 18px;
      font-weight: bold;
      transition: 0.3s;
    }

    nav a:hover {
      text-decoration: underline;
      font-size: 20px;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Conteúdo */
    #conteudo {
      display: none;
    }

    section {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 32px;
    }
  </style>
</head>
<body>
  <!-- Tela de Login -->
  <div id="login-box">
    <div class="login-card">
      <h2>Login</h2>
      <input type="text" id="user" placeholder="Usuário">
      <input type="password" id="pass" placeholder="Senha">
      <button onclick="login()">Entrar</button>
      <p id="msg" style="color:red;"></p>
    </div>
  </div>

  <!-- Conteúdo com Menu -->
  <div id="conteudo">
    <nav>
      <a href="#home">🏠 Início</a>
      <a href="#sobre">ℹ️ Sobre</a>
      <a href="#scripts">💻 Scripts</a>
      <a href="#contato">📩 Contato</a>
    </nav>

    <section id="home">Bem-vindo ao meu site 🚀</section>
    <section id="sobre">Sobre mim ✨</section>
    <section id="scripts">Scripts disponíveis ⚡</section>
    <section id="contato">Entre em contato 📱</section>
  </div>

  <script>
    function login() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      // 🔒 Usuário e senha fixos (troque aqui)
      const USERNAME = "admin";
      const PASSWORD = "12345";

      if (user === USERNAME && pass === PASSWORD) {
        document.getElementById("login-box").style.display = "none";
        document.getElementById("conteudo").style.display = "block";
      } else {
        document.getEle mentById("msg").innerText = "Usuário ou senha incorretos!";
      }
    }
  </script>
</body>
</html>

<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login + Menu</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f4f6;
    }

    /* Tela de login */
    #login-box {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 300px;
      width: 100%;
    }

    .login-card input {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 90%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .login-card button {
      background: #2d72d9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-card button:hover {
      background: #1a4fa3;
    }

    /* Barra do menu */
    nav {
      width: 100%;
      padding: 15px 0;
      text-align: center;
      background: linear-gradient(270deg, #ff6b6b, #f7d794, #1dd1a1, #54a0ff, #5f27cd);
      background-size: 1000% 1000%;
      animation: gradientShift 12s ease infinite;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 20px;
      font-size: 18px;
      font-weight: bold;
      transition: 0.3s;
    }

    nav a:hover {
      text-decoration: underline;
      font-size: 20px;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Conteúdo */
    #conteudo {
      display: none;
    }

    section {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 32px;
    }
  </style>
</head>
<body>
  <!-- Tela de Login -->
  <div id="login-box">
    <div class="login-card">
      <h2>Login</h2>
      <input type="text" id="user" placeholder="Usuário">
      <input type="password" id="pass" placeholder="Senha">
      <button onclick="login()">Entrar</button>
      <p id="msg" style="color:red;"></p>
    </div>
  </div>

  <!-- Conteúdo com Menu -->
  <div id="conteudo">
    <nav>
      <a href="#home">🏠 Início</a>
      <a href="#sobre">ℹ️ Sobre</a>
      <a href="#scripts">💻 Scripts</a>
      <a href="#contato">📩 Contato</a>
    </nav>

    <section id="home">Bem-vindo ao meu site 🚀</section>
    <section id="sobre">Sobre mim ✨</section>
    <section id="scripts">Scripts disponíveis ⚡</section>
    <section id="contato">Entre em contato 📱</section>
  </div>

  <script>
    function login() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      // 🔒 Usuário e senha fixos (troque aqui)
      const USERNAME = "admin";
      const PASSWORD = "12345";

      if (user === USERNAME && pass === PASSWORD) {
        document.getElementById("login-box").style.display = "none";
        document.getElementById("conteudo").style.display = "block";
      } else {
        document.getElementById("msg").innerText = "Usuário ou senha incorretos!";
      }
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login + Menu</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f4f6;
    }

    /* Tela de login */
    #login-box {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 300px;
      width: 100%;
    }

    .login-card input {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 90%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .login-card button {
      background: #2d72d9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-card button:hover {
      background: #1a4fa3;
    }

    /* Barra do menu */
    nav {
      width: 100%;
      padding: 15px 0;
      text-align: center;
      background: linear-gradient(270deg, #ff6b6b, #f7d794, #1dd1a1, #54a0ff, #5f27cd);
      background-size: 1000% 1000%;
      animation: gradientShift 12s ease infinite;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin: 0 20px;
      font-size: 18px;
      font-weight: bold;
      transition: 0.3s;
    }

    nav a:hover {
      text-decoration: underline;
      font-size: 20px;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Conteúdo */
    #conteudo {
      display: none;
    }

    section {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 32px;
    }
  </style>
</head>
<body>
  <!-- Tela de Login -->
  <div id="login-box">
    <div class="login-card">
      <h2>Login</h2>
      <input type="text" id="user" placeholder="Usuário">
      <input type="password" id="pass" placeholder="Senha">
      <button onclick="login()">Entrar</button>
      <p id="msg" style="color:red;"></p>
    </div>
  </div>

  <!-- Conteúdo com Menu -->
  <div id="conteudo">
    <nav>
      <a href="#home">🏠 Início</a>
      <a href="#sobre">ℹ️ Sobre</a>
      <a href="#scripts">💻 Scripts</a>
      <a href="#contato">📩 Contato</a>
    </nav>

    <section id="home">Bem-vindo ao meu site 🚀</section>
    <section id="sobre">Sobre mim ✨</section>
    <section id="scripts">Scripts disponíveis ⚡</section>
    <section id="contato">Entre em contato 📱</section>
  </div>

  <script>
    function login() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      // 🔒 Usuário e senha fixos (troque aqui)
      const USERNAME = "admin";
      const PASSWORD = "12345";

      if (user === USERNAME && pass === PASSWORD) {
        document.getElementById("login-box").style.display = "none";
        document.getElementById("conteudo").style.display = "block";
      } else {
        document.getElementById("msg").innerText = "Usuário ou senha incorretos!";
      }
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Menu com Login</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f4f6;
    }

    /* Barra do menu */
    nav {
      width: 100%;
      padding: 15px 0;
      text-align: center;
      background: linear-gradient(270deg, #ff6b6b, #f7d794, #1dd1a1, #54a0ff, #5f27cd);
      background-size: 1000% 1000%;
      animation: gradientShift 12s ease infinite;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    nav a, nav button {
      color: white;
      text-decoration: none;
      margin: 0 15px;
      font-size: 18px;
      font-weight: bold;
      transition: 0.3s;
      background: none;
      border: none;
      cursor: pointer;
    }

    nav a:hover, nav button:hover {
      text-decoration: underline;
      font-size: 20px;
    }

    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Modal de login */
    #login-modal {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.5);
      justify-content: center;
      align-items: center;
    }

    .login-card {
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.3);
      text-align: center;
      max-width: 300px;
      width: 100%;
      animation: fadeIn 0.3s;
    }

    .login-card input {
      display: block;
      margin: 10px auto;
      padding: 10px;
      width: 90%;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    .login-card button {
      background: #2d72d9;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .login-card button:hover {
      background: #1a4fa3;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    /* Conteúdo */
    section {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 32px;
    }
  </style>
</head>
<body>
  <!-- Menu -->
  <nav>
    <a href="#home">🏠 Início</a>
    <a href="#sobre">ℹ️ Sobre</a>
    <a href="#scripts">💻 Scripts</a>
    <a href="#contato">📩 Contato</a>
    <button id="loginBtn" onclick="abrirLogin()">🔑 Login</button>
  </nav>

  <!-- Modal de Login -->
  <div id="login-modal">
    <div class="login-card">
      <h2>Login</h2>
      <input type="text" id="user" placeholder="Usuário">
      <input type="password" id="pass" placeholder="Senha">
      <button onclick="login()">Entrar</button>
      <p id="msg" style="color:red;"></p>
    </div>
  </div>

  <!-- Conteúdo -->
  <section id="home">Bem-vindo ao meu site 🚀</section>
  <section id="sobre">Sobre mim ✨</section>
  <section id="scripts" style="display:none;">Scripts disponíveis ⚡</section>
  <section id="contato">Entre em contato 📱</section>

  <script>
    function abrirLogin() {
      document.getElementById("login-modal").style.display = "flex";
    }

    function login() {
      const user = document.getElementById("user").value;
      const pass = document.getElementById("pass").value;

      // 🔒 Usuário e senha fixos
      const USERNAME = "admin";
      const PASSWORD = "12345";

      if (user === USERNAME && pass === PASSWORD) {
        document.getElementById("login-modal").style.display = "none";
        document.getElementById("scripts").style.display = "flex";
        document.getElementById("loginBtn").style.display = "none"; // esconder botão de login
      } else {
        document.getElementById("msg").innerText = "Usuário ou senha incorretos!";
      }
    }

    // Fechar modal clicando fora
    window.onclick = function(e) {
      const modal = document.getElementById("login-modal");
      if (e.target === modal) {
        modal.style.display = "none";
      }
    }
  </script>
</body>
</html>
