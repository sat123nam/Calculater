# Calculater
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Stylish Calculator</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #0a4946; /* Dark teal background */
      color: #ffffff; /* White text */
    }

    #calculator {
      text-align: center;
      margin: auto;
      background-color: #1e9282; /* Teal */
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle box shadow */
    }

    input {
      width: calc(100% - 20px);
      padding: 10px;
      margin: 10px 0;
      font-size: 18px;
      border: none;
      border-radius: 5px;
      background-color: #2eb8b2; /* Light teal */
      color: #ffffff; /* White text */
    }

    button {
      width: 48px;
      height: 48px;
      margin: 5px;
      font-size: 18px;
      cursor: pointer;
      border: none;
      border-radius: 5px;
      background-color: #147568; /* Dark teal for operators */
      color: #ffffff; /* White text */
    }

    button:hover {
      background-color: #0d4c49; /* Darker teal on hover */
    }

    h1 {
      text-align: center;

      
      color: #ffffff; /* White text */
      margin-bottom: auto;
    }

    .para {
      text-align: center;
      margin-bottom: 300px;
      margin-right: 400px;
      
    }
  </style>
</head>
<body>
  <h1>Calculator</h1>
  <p class="para">calculations with <br>
     style Lorem ipsum dolor sit amet <br>
     consectetur adipisicing elit. Ex, vitae.</p>
  <div id="calculator">
    <input type="text" id="display" disabled>
    <br>
    <button onclick="clearDisplay()">C</button>
    <button onclick="appendCharacter('/')">/</button>
    <button onclick="appendCharacter('*')">*</button>
    <button onclick="appendCharacter('-')">-</button>
    <br>
    <button onclick="appendCharacter('7')">7</button>
    <button onclick="appendCharacter('8')">8</button>
    <button onclick="appendCharacter('9')">9</button>
    <button onclick="appendCharacter('+')">+</button>
    <br>
    <button onclick="appendCharacter('4')">4</button>
    <button onclick="appendCharacter('5')">5</button>
    <button onclick="appendCharacter('6')">6</button>
    <button onclick="calculate()">=</button>
    <br>
    <button onclick="appendCharacter('1')">1</button>
    <button onclick="appendCharacter('2')">2</button>
    <button onclick="appendCharacter('3')">3</button>
    <button onclick="appendCharacter('0')">0</button>
  </div>

  <script>
    function clearDisplay() {
      document.getElementById('display').value = '';
    }

    function appendCharacter(char) {
      document.getElementById('display').value += char;
    }

    function calculate() {
      try {
        document.getElementById('display').value = eval(document.getElementById('display').value);
      } catch (error) {
        document.getElementById('display').value = 'Error';
      }
    }
  </script>
</body>
</html>
