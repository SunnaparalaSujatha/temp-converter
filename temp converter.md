<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <div class="input-container">
            <input type="number" id="celsiusInput" placeholder="Enter Celsius"><br>
            <button id="convertButton">Convert</button>
        </div>
        <div class="result" id="result"></div>
    </div>
    <style>
    body {
        font-family: Arial, sans-serif;
        background-color: #f4f4f4;
        margin: 0;
        padding: 0;
        background-image: url("Nature.jpg");
        background-size: cover;
        background-position: center;

    }
    
    .container {
        background-color: hwb(36 65% 4%);
        max-width: 400px;
        margin: 20px auto;
        padding: 20px;
        border-radius: 5px;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
        height: 250px;
        opacity: 0.7;
    }
    
    h1 {
        text-align: center;
    }
    
    .input-container {
        text-align: center;
    }
    
    input {
        padding: 10px;
        width: 80%;
        border: 1px solid #ccc;
        border-radius: 5px;
        margin-bottom: 20px;
    }
    
    button {
        padding: 10px 20px;
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }
    
    .result {
        text-align: center;
        font-size: 20px;
        margin-top: 20px;
    }
</style>
    <script src="script.js"></script>
    <script>
        document.addEventListener("DOMContentLoaded", function () {
    const celsiusInput = document.getElementById("celsiusInput");
    const convertButton = document.getElementById("convertButton");
    const resultDiv = document.getElementById("result");

    convertButton.addEventListener("click", function () {
        const celsius = parseFloat(celsiusInput.value);

        if (!isNaN(celsius)) {
            const fahrenheit = (celsius * 9/5) + 32;
            resultDiv.innerText = ${celsius}°C = ${fahrenheit.toFixed(2)}°F;
        } else {
            resultDiv.innerText = "Please enter a valid temperature in Celsius.";
        }
    });
});

    </script>
</body>
</html>
