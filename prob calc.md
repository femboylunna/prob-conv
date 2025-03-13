<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Percentage to 1 in X Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
        }
        input, button {
            font-size: 18px;
            margin: 10px;
            padding: 5px;
        }
    </style>
</head>
<body>
    <h2>Convert Percentage to "1 in X" Odds</h2>
    <input type="number" id="percentage" placeholder="Enter percentage" step="any">
    <button onclick="convert()">Convert</button>
    <p id="result"></p>

    <script>
        function convert() {
            let percentage = parseFloat(document.getElementById('percentage').value);
            if (isNaN(percentage) || percentage <= 0) {
                document.getElementById('result').innerText = "Please enter a valid percentage.";
                return;
            }
            let oneInX = 1 / (percentage / 100);
            document.getElementById('result').innerText = `1 in ${Math.round(oneInX).toLocaleString()}`;
        }
    </script>
</body>
</html>
