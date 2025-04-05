<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>gmail | login Portal</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background: linear-gradient(135deg, #4facfe, #00f2fe);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .login-container {
      background-color: #fff;
      padding: 30px 40px;
      border-radius: 15px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
      width: 100%;
      max-width: 400px;
    }

    .login-container h2 {
      text-align: center;
      margin-bottom: 25px;
      color: #333;
    }

    label {
      display: block;
      margin-bottom: 6px;
      font-weight: bold;
    }

    input[type="email"],
    input[type="password"] {
      width: 100%;
      padding: 12px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 16px;
      transition: 0.3s;
    }

    input:focus {
      border-color: #4facfe;
      outline: none;
    }

    button {
      width: 100%;
      padding: 12px;
      background-color: #4facfe;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background-color: #00c6fb;
    }
  </style>
</head>
<body>
  <div class="login-container">
    <h2>gmail Login</h2>
    <form onsubmit="handleLogin(event)">
      <label for="email">Email Address</label>
      <input type="email" id="email" required />

      <label for="password">Password</label>
      <input type="password" id="password" required />

      <button type="submit">Login</button>
    </form>
  </div>

  <script>
    function handleLogin(event) {
      event.preventDefault();
      const email = document.getElementById("email").value;
      const password = document.getElementById("password").value;

      localStorage.setItem("eduEmail", email);
      localStorage.setItem("eduPass", password);

      window.location.href = "welcome.html";
    }
  </script>
</body>
</html>
