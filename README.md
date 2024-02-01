<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BubuSearch</title>
    <style>
        body {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }

        form {
            text-align: center;
        }

        #responseContainer {
            margin-top: 20px;
            text-align: center;
        }
    </style>
</head>
<body>

    <div>
        <h1>Welcome to BubuSearch</h1>
        
        <form onsubmit="return displayResponse()">
            <input type="text" id="searchInput" name="searchInput" required>
            <button type="submit">Search</button>
        </form>

        <div id="responseContainer"></div>
    </div>

    <script>
        function displayResponse() {
            // Get the input value
            var userInput = document.getElementById('searchInput').value;

            // Display the fixed response
            var responseContainer = document.getElementById('responseContainer');
            responseContainer.innerHTML = '<p>Bubu, it\'s Dudu, I love you</p>';

            // Prevent the form from submitting and refreshing the page
            return false;
        }

        // Handle Enter key press
        document.getElementById('searchInput').addEventListener('keypress', function (e) {
            if (e.key === 'Enter') {
                displayResponse();
            }
        });
    </script>

</body>
</html>
