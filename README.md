# simplecaculator
making a webpage of a simple calculator with basic operators.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        body {
            font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            background-color: #f2f2f2;
        }
        h1 {
            text-align: center;
            margin-top: 50px;letter-spacing: 10px;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.2);
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%,-50%);
            
        }
        .row{display: flex;
            flex-wrap: row wrap;justify-content: center;
        }
        input[type="text"] {
            padding: 10px;
            margin: 10px;
            border-radius: 5px;
            border: none;
            box-shadow: 0 0 5px rgba(0,0,0,0.2);
            font-size: 24px;
            text-align: right;
            width: 630px;
            display:inline;
            justify-content: center;
            flex-wrap: wrap;
            

        }
        input[type="submit"] {
            padding: 10px 50px;
            margin: 10px;
            border-radius: 5px;
            border: none;
            background-color: #4CAF50;
            color: #fff;
            font-size: 24px;
            cursor: pointer;
            text-align:justify;

        }
        #result {
            padding: 10px ;
            margin: 10px;
            border-radius: 5px;
            border: none;
            box-shadow: 0 0 5px rgba(0,0,0,0.2);
            font-size: 24px;
            text-align: right;
        }
    </style>
</head>
<body>
    <h1>Calculator</h1>
    <div class="container">
        <input type="text" id="num1" >
        <br>
        <input type="text" id="num2" >
        <br>
        <div class="row">
        <input type="submit" value="+" onclick="add()">
        <input type="submit" value="-" onclick="subtract()">
        <input type="submit" value="*" onclick="multiply()">
        <input type="submit" value="/" onclick="divide()">
        <input type="submit" value="AC"onclick="allclear()">
        </div>
        <br>
        <p id="result">Result</p>
    </div>
    <script>
        function add() {
            var num1 = parseFloat(document.getElementById("num1").value);
            var num2 = parseFloat(document.getElementById("num2").value);
            var result = num1 + num2;
            document.getElementById("result").innerHTML = num1 + " + " + num2 + " = " + result;
        }
        function subtract() {
            var num1 = parseFloat(document.getElementById("num1").value);
            var num2 = parseFloat(document.getElementById("num2").value);
            var result = num1 - num2;
            document.getElementById("result").innerHTML = num1 + " - " + num2 + " = " + result;
        }
        function multiply() {
            var num1 = parseFloat(document.getElementById("num1").value);
            var num2 = parseFloat(document.getElementById("num2").value);
            var result = num1 * num2;
            document.getElementById("result").innerHTML = num1 + " * " + num2 + " = " + result;
        }
        function divide() {
            var num1 = parseFloat(document.getElementById("num1").value);
            var num2 = parseFloat(document.getElementById("num2").value);
            if(num2 == 0) {
                document.getElementById("result").innerHTML = "除數不能為零";
            } else {
                var result = num1 / num2;
                document.getElementById("result").innerHTML = num1 + " / " + num2 + " = " + result;
            }
        }
        function allclear() {
            document.getElementById("num1").value = "0";
            document.getElementById("num2").value = "0";
            document.getElementById("result").innerHTML = "0";            
        }
    </script>
</body>
</html>
