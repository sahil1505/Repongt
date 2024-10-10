# Repongt

------------------TABLE-------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multiplication Table</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <style>
        #result {
            display: none; /* Initially hidden */
            margin-top: 10px;
        }
    </style>
</head>
<body>

Enter a number: <input type="number" id="numberInput"><br><br>
<button id="generateTable">Generate Table</button>
<div id="result"></div>

<script>
    $(document).ready(function(){
        $("#generateTable").click(function(){
            var number = parseInt($("#numberInput").val());
            var tableHtml = "<table border='1'><tr><th>Multiplier</th><th>Result</th></tr>";

            for (var i = 1; i <= 10; i++) {
                tableHtml += "<tr><td>" + number + " x " + i + "</td><td>" + (number * i) + "</td></tr>";
            }
            tableHtml += "</table>";

            $("#result").html(tableHtml).slideDown(); // Display the table with slide down effect
        });
    });
</script>

</body>
</html>

------ACCEPTING 2 NUMBERS AND DISPLAY BETWEEN NOS.-----------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Display Numbers Between m and n</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <style>
        #result {
            display: none; /* Initially hidden */
            margin-top: 10px;
        }
    </style>
</head>
<body>

Enter the first number (m): <input type="number" id="numberM"><br><br>
Enter the second number (n): <input type="number" id="numberN"><br><br>
<button id="displayNumbers">Display Numbers</button>
<p id="result"></p>

<script>
    $(document).ready(function(){
        $("#displayNumbers").click(function(){
            var m = parseInt($("#numberM").val());
            var n = parseInt($("#numberN").val());

            if (m < n) {
                var numbers = "";
                for (var i = m + 1; i < n; i++) {
                    numbers += i + " ";
                }
                $("#result").text("Numbers between " + m + " and " + n + ": " + numbers).slideDown();
            } else {
                $("#result").text("Please ensure that m is less than n.").slideDown();
            }
        });
    });
</script>

</body>
</html>

----------------COUNTDOWN---------------;

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Countdown Timer</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <style>
        #result {
            display: none; /* Initially hidden */
            margin-top: 10px;
            font-size: 24px;
        }
    </style>
</head>
<body>

Enter countdown time in seconds: <input type="number" id="countdownInput"><br><br>
<button id="startCountdown">Start Countdown</button>
<div id="result"></div>

<script>
    $(document).ready(function(){
        $("#startCountdown").click(function(){
            var countdownTime = parseInt($("#countdownInput").val());
            var display = $("#result");
            display.show();
            
            var countdown = setInterval(function() {
                if (countdownTime >= 0) {
                    display.text("Time remaining: " + countdownTime + " seconds");
                    countdownTime--;
                } else {
                    clearInterval(countdown);
                    display.text("Time's up!");
                }
            }, 1000);
        });
    });
</script>

</body>
</html>

--------SUM OF TWO USING SLIDE DOWN-----------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <title>Document</title>
    <style>
        #result {
            display: none;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    Enter First Number: <input type="number", id="number1"><br><br>
    Enter Second Number: <input type="number", id="number2"><br><br>
    <button id="calculateSum">Calculate Sum</button>
    <p id="result"></p>
    <script>
        $(document).ready(function() {
            $('#calculateSum').click(function() {
                var num1 = parseFloat($('#number1').val());
                var num2 = parseFloat($('#number2').val());
                var sum = num1 + num2;
                $("#result").text("The sum is: " + sum).slideDown();
            });
        });
    </script>
</body>
</html>


------------DATE AND TIME USING SLIDE DOWN--------------- 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <title>Document</title>
</head>
<body>
    <button id="showDateTime">Show Current Date and Time</button>
    <p id="dateTimeDisplay"></p>
    <script>
        $(document).ready(function(){
            $("#showDateTime").click(function(){
                var date = new Date();
                $("#dateTimeDisplay").text("Current Date and Time: " + date).slideDown();
        });
    });
    </script>
</body>
</html>

---------------SUM OF TWO USING ALERT-------------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <title>Document</title>
</head>
<body>
    Enter First Number: <input type="number", id="number1"><br><br>
    Enter Second Number: <input type="number", id="number2"><br><br>
    <button id="calculateSum">Calculate Sum</button>
    <script>
        $(document).ready(function(){
            $("#calculateSum").click(function(){
                var num1 = parseFloat($("#number1").val());
                var num2 = parseFloat($("#number2").val());
                var sum = num1 + num2;
                alert("The sum is: " + sum);
            });
        });
    </script>
</body>
</html>

----------CURRENT DATE ANDD TIME USING ALERT--------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <title>Document</title>
</head>
<body>
    <button id="showDateTime">Show Current Date and Time</button>
    <script>
        $(document).ready(function(){
            $("#showDateTime").click(function(){
                var date = new Date();
                alert("Current Date and Time: " + date);
            });
        });
    </script>
</body>
</html>


----------------HELLO SEPTEMBER----------------;;

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <title>Document</title>
</head>
<body>
    <button id="myButton">Click Me</button>
    <p id="message"></p>
    <script>
        $(document).ready(function(){
            $('#myButton').click(function(){
                $("#message").text("Hello September");
        });
    });
    </script>
</body>
</html>

-----------------CURRENT DATE AND TIME--------------------------------

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <title>Document</title>
</head>
<body>
    <button id="showDateTime">Show Current Date and Time</button>
    <p id="dateTimeDisplay"></p>
    <script>
        $(document).ready(function(){
            $("#showDateTime").click(function(){
                var date = new Date();
                $("#dateTimeDisplay").text(date);
            });
        });
    </script>
</body>
</html>


