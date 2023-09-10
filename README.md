# simplecaculator
making a webpage of a simple calculator with basic operators.


    
    
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
