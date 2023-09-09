# Temp_Converter
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .container {
            margin: 20px auto;
            width: 300px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <label for="celsius">Enter Temperature in Celsius:</label>
        <input type="number" id="celsius" placeholder="Enter Celsius">
        <br><br>
        <button onclick="convertTemperature()">Convert</button>
        <br><br>
        <p id="result"></p>
    </div>
  
    <script>
        function convertTemperature() {
            const celsiusInput = document.getElementById("celsius").value;
            const celsius = parseFloat(celsiusInput); 
            if (isNaN(celsius)) {
                alert("Please enter a valid number for Celsius.");
                return;
            }
            const fahrenheit = (celsius * 9/5) + 32;
            document.getElementById("result").textContent = `${celsius}°C is equal to ${fahrenheit}°F`;
        }
    </script>
</body>
</html>
