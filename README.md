<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initialscale=1.0">
<title>Simple Dynamic Calculator</title>
<style>
body { font-family: Arial, sans-serif; padding: 40px;
background-color: #f4f7f6; display: flex; justify-content: center; }
.calc-box { background: white; padding: 30px; border-radius:
8px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); width: 320px; text-align:
center; }
h2 { color: #2c3e50; margin-bottom: 20px; }
input, select, button { width: 100%; padding: 10px; margin:
10px 0; border: 1px solid #ccc; border-radius: 4px; font-size: 1rem;
box-sizing: border-box; }
button { background-color: #3498db; color: white; border:
none; font-weight: bold; cursor: pointer; transition: 0.2s; }
button:hover { background-color: #2980b9; }
.result-display { margin-top: 20px; padding: 15px; backgroundcolor: #ecf0f1; border-radius: 4px; font-size: 1.2rem; font-weight:
bold; color: #2c3e50; min-height: 50px; display: flex; align-items:
center; justify-content: center; }
</style>
</head>
<body>
<div class="calc-box">
<h2>JS Calculator</h2>
<input type="number" id="num1" placeholder="Enter first
number">
<select id="operator">
<option value="add">Add (+)</option>
<option value="subtract">Subtract (-)</option>
<option value="multiply">Multiply (&times;)</option>
<option value="divide">Divide (&divide;)</option>
</select>
<input type="number" id="num2" placeholder="Enter second
number">
<button id="calc-btn">Calculate</button>
<div class="result-display" id="result-output">Result will
appear here</div>
</div>
<script src="script.js"></script>
</body>
</html>
const calculatorOperations = {
add: function(a, b) { return a + b; },
subtract: function(a, b) { return a - b; },
multiply: function(a, b) { return a * b; },
divide: function(a, b) {
return b === 0 ? "Error (Divide by 0)" : a / b;
}
};
const calculateButton = document.getElementById("calc-btn");
const resultOutput = document.getElementById("result-output");
function performCalculation() {
const number1 = parseFloat(document.getElementById("num1").value);
const number2 = parseFloat(document.getElementById("num2").value);
const selectedOp = document.getElementById("operator").value;
if (isNaN(number1) || !isNaN(number2) === false) {
resultOutput.textContent = "Please enter valid numbers!";
resultOutput.style.color = "#e74c3c";
return;
}
let finalResult;
if (selectedOp === "add") {
finalResult = calculatorOperations.add(number1, number2);
} else if (selectedOp === "subtract") {
finalResult = calculatorOperations.subtract(number1, number2);
} else if (selectedOp === "multiply") {
finalResult = calculatorOperations.multiply(number1, number2);
} else if (selectedOp === "divide") {
finalResult = calculatorOperations.divide(number1, number2);
}
resultOutput.textContent = `Result = ${finalResult}`;
resultOutput.style.color = "#27ae60";
}
calculateButton.addEventListener("click", performCalculation);
