## simple-calculator
## DATE:26/08/2025
## REG NO:212223040029
## AIM:
Create a Simple Calculator using HTML, CSS, and JavaScript.
## PROCEDURE:
1. Take two numbers as input.

2. Let the user choose an operation (Add, Subtract, Multiply, Divide).

3. Display the result on the page when the user clicks a button.
## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f0f2f5;
    }
    .calculator {
      background: #fff;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      width: 300px;
      text-align: center;
    }
    h2 {
      margin-bottom: 15px;
    }
    input, select, button {
      margin: 8px 0;
      padding: 10px;
      width: 90%;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    button {
      background: #4CAF50;
      color: white;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #45a049;
    }
    .result {
      margin-top: 15px;
      font-size: 18px;
      font-weight: bold;
      color: #333;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <h2>Simple Calculator</h2>
    <input type="number" id="num1" placeholder="Enter first number">
    <input type="number" id="num2" placeholder="Enter second number">

    <select id="operation">
      <option value="add">Add (+)</option>
      <option value="subtract">Subtract (-)</option>
      <option value="multiply">Multiply (×)</option>
      <option value="divide">Divide (÷)</option>
    </select>

    <button onclick="calculate()">Calculate</button>
    <div class="result" id="result"></div>
  </div>

  <script>
    function calculate() {
      let num1 = parseFloat(document.getElementById("num1").value);
      let num2 = parseFloat(document.getElementById("num2").value);
      let operation = document.getElementById("operation").value;
      let result = "";

      if (isNaN(num1) || isNaN(num2)) {
        result = "⚠️ Please enter both numbers!";
      } else {
        switch (operation) {
          case "add":
            result = num1 + num2;
            break;
          case "subtract":
            result = num1 - num2;
            break;
          case "multiply":
            result = num1 * num2;
            break;
          case "divide":
            result = num2 !== 0 ? (num1 / num2) : "⚠️ Cannot divide by zero!";
            break;
        }
      }

      document.getElementById("result").innerText = "Result: " + result;
    }
  </script>
</body>
</html>
```
## OUTPUT:
<img width="1902" height="1078" alt="image" src="https://github.com/user-attachments/assets/0dcf3558-9c4b-4fd8-bb18-b0591587ce31" />
## RESULT:
 Simple Calculator using HTML, CSS, and JavaScript is implemented successsfully.

