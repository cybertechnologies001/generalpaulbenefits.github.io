<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CHASE BANK</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f2f5;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #0a2c63;
      color: white;
      padding: 20px;
      text-align: center;
    }
    .container {
      max-width: 600px;
      margin: 40px auto;
      background-color: white;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 10px;
      padding: 30px;
    }
    .section {
      margin-bottom: 20px;
    }
    .label {
      font-weight: bold;
    }
    .value {
      margin-left: 10px;
      color: #333;
    }
    .login-form {
      margin-bottom: 30px;
    }
    .login-form input[type="text"],
    .login-form input[type="password"],
    select {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .login-form input[type="submit"],
    #verification-form input[type="submit"] {
      background-color: #0a2c63;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      cursor: pointer;
    }
    .hidden {
      display: none;
    }
    ul.value {
      list-style: none;
      padding: 0;
    }
    ul.value li {
      padding: 5px 0;
    }
  </style>
  <script>
    function login(event) {
      event.preventDefault();
      const username = document.getElementById('username').value;
      const password = document.getElementById('password').value;
      if (username === 'paul' && password === 'secure123') {
        document.getElementById('login-form').classList.add('hidden');
        document.getElementById('account-info').classList.remove('hidden');
      } else {
        alert('Invalid credentials. Try username: paul and password: secure123');
      }
    }
  </script>
</head>
<body>
  <header>
    <h1>CHASE BANK</h1>
  </header>
  <div class="container">
    <form id="login-form" class="login-form" onsubmit="login(event)">
      <h2>Login</h2>
      <label for="username">Username:</label>
      <input type="text" id="username" name="username" required />
      <label for="password">Password:</label>
      <input type="password" id="password" name="password" required />
      <input type="submit" value="Login" />
    </form>

    <div id="account-info" class="hidden">
      <div class="section">
        <div class="label">Owner Name:</div>
        <div class="value">PAUL JOSEPH LACAMERA</div>
      </div>
      <div class="section">
        <div class="label">Account Balance:</div>
        <div class="value">$356,000</div>
      </div>
      <div class="section">
        <div class="label">Beneficiary:</div>
        <div class="value">NANCY SHELNUTT</div>
      </div>
      <div class="section">
        <div class="label">Transaction History:</div>
        <ul class="value">
          <li>+ $2,000 - Paycheck Deposit (June 20, 2025)</li>
          <li>- $150 - Grocery Store Purchase (June 18, 2025)</li>
          <li>- $1,000 - Rent Payment (June 15, 2025)</li>
          <li>+ $500 - Refund (June 10, 2025)</li>
          <li>- $300 - Utility Bill (June 5, 2025)</li>
        </ul>
      </div>
      <div class="section">
        <div class="label">Beneficiary Verification</div>
        <form id="verification-form">
          <label for="id-type">Select ID Type:</label>
          <select id="id-type" name="id-type" required>
            <option value="">-- Select --</option>
            <option value="passport">Passport</option>
            <option value="driver-license">Driver's License</option>
            <option value="national-id">National ID</option>
          </select>

          <label for="id-number">Enter ID Number:</label>
          <input type="text" id="id-number" name="id-number" required />

          <label for="security-code">Security Code:</label>
          <input type="password" id="security-code" name="security-code" required />

          <input type="submit" value="Verify" />
        </form>
      </div>
    </div>
  </div>
</body>
</html>
