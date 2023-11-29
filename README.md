<!DOCTYPE html>
<html>
<head>
  <title>Password Generator</title>
</head>
<body>
  <h1>Password Generator</h1>
  <label for="length">Password Length:</label>
  <input type="number" id="length" min="8" max="20" value="12">
  <button onclick="generatePassword()">Generate Password</button>
  <p id="password"></p>

  <script src="passwordGenerator.js"></script>
</body>
</html>

JavaScript (passwordGenerator.js):
function generatePassword() {
  const length = document.getElementById('length').value;
  const password = generateRandomPassword(length);
  document.getElementById('password').textContent = password;
}

function generateRandomPassword(length) {
  const charset = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789!@#$%^&*()-_=+';
  let password = '';
  for (let i = 0; i < length; i++) {
    const randomIndex = Math.floor(Math.random() * charset.length);
    password += charset[randomIndex];
  }
  return password;
}
