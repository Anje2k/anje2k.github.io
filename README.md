<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>First Calculator</title>
</head>
<body>
  <h1>Look, it's a calculator!</h1>
  <p>This is a very semi-double-basic-ish webpage hosted on GitHub Pages.</p> # CAn I add stuff heree?
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
</table>

</body>
</html>


<form id="myForm">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" placeholder="Enter your name">
  <br>
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" placeholder="Enter your email">
  <br>
  <button type="submit">Submit</button>
</form>

<script>
  const form = document.getElementById("myForm");

  form.addEventListener("submit", function(event) {
    const name = document.getElementById("name").value;
    const email = document.getElementById("email").value;

    if (name === "" || email === "") {
      alert("Please fill in all fields!");
      event.preventDefault(); // Prevent form submission
    } else {
      
    }
  });
</script>

