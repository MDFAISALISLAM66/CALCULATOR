# CALCULATOR
<!DOCTYPE html> 
<html> 
<head> 
  <title>Simple Calculator</title> 
  <style> 
    body { 
      font-family: Arial, sans-serif; 
    } 
    .calculator { 
      width: 200px; 
      border: 1px solid #ccc; 
      padding: 10px; 
      margin: 0 auto; 
    } 
    .calculator input[type="text"] { 
      width: 100%; 
      margin-bottom: 10px; 
    } 
    .calculator input[type="button"] { 
      width: 48%; 
      padding: 10px; 
      margin: 2px; 
      border: 1px solid #ccc; 
      cursor: pointer; 
    } 
    .calculator input[type="button"]:hover { 
      background-color: #f0f0f0; 
    } 
  </style> 
</head> 
<body> 
 
<div class="calculator"> 
  <input type="text" id="display" disabled> 
  <br> 
  <input type="button" value="1" onclick="appendToDisplay('1')"> 
  <input type="button" value="2" onclick="appendToDisplay('2')"> 
  <input type="button" value="3" onclick="appendToDisplay('3')"> 
  <input type="button" value="+" onclick="appendToDisplay('+')"> 
  <br> 
  <input type="button" value="4" onclick="appendToDisplay('4')"> 
  <input type="button" value="5" onclick="appendToDisplay('5')"> 
  <input type="button" value="6" onclick="appendToDisplay('6')"> 
  <input type="button" value="-" onclick="appendToDisplay('-')"> 
  <br> 
  <input type="button" value="7" onclick="appendToDisplay('7')"> 
  <input type="button" value="8" onclick="appendToDisplay('8')"> 
  <input type="button" value="9" onclick="appendToDisplay('9')"> 
  <input type="button" value="" onclick="appendToDisplay('')"> 
  <br> 
  <input type="button" value="0" onclick="appendToDisplay('0')"> 
  <input type="button" value="." onclick="appendToDisplay('.')"> 
  <input type="button" value="/" onclick="appendToDisplay('/')"> 
  <input type="button" value="C" onclick="clearDisplay()"> 
  <br> 
  <input type="button" value="=" onclick="calculate()"> 
</div> 
 
<script> 
  function appendToDisplay(value) { 
    document.getElementById('display').value += value; 
  } 
 
  function clearDisplay() { 
    document.getElementById('display').value = ''; 
  } 
 
  function calculate() { 
    var result = eval(document.getElementById('display').value); 
    document.getElementById('display').value = result; 
  } 
</script> 
 
</body> 
</html>
