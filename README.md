<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>First Calculator</title>
</head>
<body>
  <h1>Look, it's a calculator!</h1>
  <p>This is a webpage calculator hosted on GitHub Pages.</p>
  <p><input type="text" id="display" value="" readonly></p>
  <table>
  <tr>
    <td><button onclick="handleNumber('7')">7</button></td>
    <td><button onclick="handleNumber('8')">8</button></td>
    <td><button onclick="handleNumber('9')">9</button></td>
    <td><button onclick="handleOperator('+')">+</button></td>
  </tr>
  <tr>
    <td><button onclick="handleNumber('4')">4</button></td>
    <td><button onclick="handleNumber('5')">5</button></td>
    <td><button onclick="handleNumber('6')">6</button></td>
    <td><button onclick="handleOperator('-')">-</button></td>
  </tr>
  <tr>
    <td><button onclick="handleNumber('1')">1</button></td>
    <td><button onclick="handleNumber('2')">2</button></td>
    <td><button onclick="handleNumber('3')">3</button></td>
    <td><button onclick="handleOperator('*')">*</button></td>    
  </tr>
  <tr>
    <td><button onclick="handleEqual()">=</button></td>
    <td><button onclick="handleNumber('0')">0</button></td>
    <td><button onclick="clearDisplay()">C</button></td>
    <td><button onclick="handleOperator('/')">/</button></td>    
  </tr>
</table>
<br>
<p> This is a <a href="aboutus.md">secret</a> page</p>

</body>
</html>



<script>

let currentNumber = "";
let previousNumber = "";
let operation = "";

function handleNumber(number) {
  currentNumber += number;
  document.getElementById("display").value = currentNumber;
}

function handleOperator(op) {
  previousNumber = currentNumber;
  currentNumber = "";
  operation = op;
}

function clearDisplay() {
  currentNumber = "";
  previousNumber = "";
  operation = "";
  document.getElementById("display").value = "";
}

function handleEqual() {
  let result = 0;
  if (operation === "+") {
    result = parseFloat(previousNumber) + parseFloat(currentNumber);
  } else if (operation === "-") {
    result = parseFloat(previousNumber) - parseFloat(currentNumber);
  } else if (operation === "*") {
    result = parseFloat(previousNumber) * parseFloat(currentNumber);
  } else if (operation === "/") {
    result = parseFloat(previousNumber) / parseFloat(currentNumber);
  }
  currentNumber = result.toString();
  document.getElementById("display").value = currentNumber;
}

</script>
