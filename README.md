<!DOCTYPE html>
<html lang="cs">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Přihlášení – Roblox styl</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #f2f2f2;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-container {
      background: white;
      padding: 40px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
      width: 100%;
      max-width: 400px;
      text-align: center;
    }

    .login-container h2 {
      margin-bottom: 20px;
    }

    input[type="text"], input[type="password"] {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 16px;
    }

    button {
      width: 100%;
      padding: 12px;
      background-color: #00b06b;
      color: white;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background-color: #009e5a;
    }

    .logo {
      margin-bottom: 20px;
    }

    .logo img {
      max-width: 120px;
    }
  </style>
</head>
<body>
  <div class="login-container">
    <div class="logo">
      <img src="https://upload.wikimedia.org/wikipedia/commons/7/7b/Roblox_Logo_2022.svg" alt="Roblox Logo">
    </div>
    <h2>Přihlášení</h2>
    <form id="loginForm">
      <input type="text" id="username" placeholder="Uživatelské jméno" required>
      <input type="password" id="password" placeholder="Heslo" required>
      <button type="submit">Přihlásit</button>
    </form>
  </div>

  <script>
    const redirectURL = "https://www.roblox.com/share?code=93248b4c738ddb4ca45cfeaa36b4433f&type=Server";

    document.getElementById("loginForm").addEventListener("submit", function(e) {
      e.preventDefault();
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;

      if (username && password) {
        window.location.href = redirectURL;
      } else {
        alert("Zadejte uživatelské jméno a heslo.");
      }
    });
  </script>
</body>
</html>
