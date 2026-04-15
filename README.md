<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Калькулятор</title>
</head>
<body style="text-align:center; font-family:sans-serif;">

<h2>Калькулятор</h2>

<input id="display" style="width:200px; height:40px; font-size:20px; text-align:right;"><br><br>

<button onclick="add('1')">1</button>
<button onclick="add('2')">2</button>
<button onclick="add('3')">3</button>
<button onclick="add('+')">+</button><br>

<button onclick="add('4')">4</button>
<button onclick="add('5')">5</button>
<button onclick="add('6')">6</button>
<button onclick="add('-')">-</button><br>

<button onclick="add('7')">7</button>
<button onclick="add('8')">8</button>
<button onclick="add('9')">9</button>
<button onclick="add('*')">*</button><br>

<button onclick="add('0')">0</button>
<button onclick="clearDisplay()">C</button>
<button onclick="calculate()">=</button>
<button onclick="add('/')">/</button>

<script>
let display = document.getElementById("display");

function add(value) {
  display.value += value;
}

function clearDisplay() {
  display.value = "";
}

function calculate() {
  try {
    display.value = eval(display.value);
  } catch {
    display.value = "Ошибка";
  }
}
</script>

</body>
</html>
