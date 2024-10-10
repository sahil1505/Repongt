# Repongt
https://tinyurl.com/3wxpketc
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


#######################################
https://repo1.maven.org/maven2/org/mongodb/mongodb-driver-sync/5.0.0/  

https://repo1.maven.org/maven2/org/mongodb/mongodb-driver-core/5.0.0/mongodb-driver-core-5.0.0.jar  

https://repo1.maven.org/maven2/org/slf4j/slf4j-api/1.7.32/slf4j-api-1.7.32.jar

https://repo1.maven.org/maven2/org/slf4j/slf4j-simple/1.7.32/slf4j-simple-1.7.32.jar

https://mvnrepository.com/artifact/org.mongodb/bson/5.0.0



/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package mongo;
import com.mongodb.client.MongoClient;
import com.mongodb.client.MongoClients;
import com.mongodb.client.MongoDatabase;
import com.mongodb.client.MongoIterable;

/**
 *
 * @author LAB1-PC27
 */
public class JavaApplication5 {
/**
* @param args the command line arguments
*/
public static void main(String[] args) {
// TODO code application logic here
String u="mongodb://localhost:27017/";
MongoClient mongoclient = MongoClients.create(u);
MongoDatabase database = mongoclient.getDatabase("admin");
System.out.println("Connected to MongoDB!!");
MongoIterable<String> databaseNames = mongoclient.listDatabaseNames();
for (String dbName:databaseNames){
System.out.println("Database Name:"+dbName);
}
mongoclient.close();
}
}

#######################################
1). Inserting and Retrieving

Source Code:

import pymongo
myclient=pymongo.MongoClient("mongodb://localhost:27017")
mydb = myclient['mydatabase']
print(myclient.list_database_names())

#getting database instance

db = myclient['mydatabase']

#create collection

coll = db['data']

#insert documents into collection

data = [{"_id":"1", "name":"Aditya", "age":"24", "city":"Mumbai"},
        {"_id":"2", "name":"Sam", "age":"23", "city":"Pune"},
        {"_id":"3", "name":"Pratham", "age":"25", "city":"Delhi"}]

res = coll.insert_many(data)
print("Data inserted...")
print(res.inserted_ids)
print("First record of the collection:")
print(coll.find_one())
print("Record whose ID is 3:")
print(coll.find_one({"_id":"3"}))

------------------------------------
2) Update Many

Source Code:
from pymongo import MongoClient
client=MongoClient('localhost', 27017)
db = client['myBase']
coll = db['MYExample4']
data = [{"_id": "401", "name": "Ram", "age": "26", "city": "hyderabad"},
{"_id": "402", "name": "Rahim", "age": "27", "city": "bangalore"},
{"_id": "403", "name": "Robert", "age": "28", "city": "mumbai"}]

#Insert data
res = coll.insert_many(data)
print("Data inserted..")
print("Documents in the collection:")

# Print documents before update
for doc1 in coll.find():
    print(doc1)

# Update document with_id "41"
coll.update_many({}, {"$set": {"city": "vishakapatanam"}})
print("Documents in the collection after update operation:")
#Print documents after update

for doc2 in coll.find():
    print(doc2)

----------------------------------

3) Delete

a). Delete one

Source Code:

from pymongo import MongoClient

client=MongoClient('localhost', 27017)
db = client['myBaseD']
coll = db['MYExample1']

data = [{"_id": "401", "name": "Ram", "age": "26", "city": "hyderabad"},
{"id": "402", "name": "Rahim", "age": "27", "city": "bangalore"},
{"_id": "403", "name": "Robert", "age": "28", "city": "mumbai"}]

#Insert data
res = coll.insert_many(data)
print("Data inserted..")
print(res.inserted_ids)

coll.delete_one({"_id":"401"})

print("documents in the collection after update operation:")
for doc2 in coll.find():
    print(doc2)
