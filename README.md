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
