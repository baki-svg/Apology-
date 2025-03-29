# Apology-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>I'm Sorry</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #ffebee; /* Light pink */
            transition: background 1s;
        }
        h1 {
            color: #d32f2f;
            font-size: 3rem;
            margin-top: 50px;
        }
        #sorryImage {
            width: 300px;
            height: auto;
            margin-top: 20px;
            border-radius: 10px;
        }
        .button-container {
            margin-top: 20px;
        }
        .choice-button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        .yes-button {
            background: #4CAF50; /* Green */
            color: white;
        }
        .no-button {
            background: #d32f2f; /* Red */
            color: white;
        }
    </style>
</head>
<body>

    <h1 id="message">I'm Really Sorry 😔</h1>
    <img id="sorryImage" src="https://raw.githubusercontent.com/baki-svg/SORRY/refs/heads/main/a386e048-6099-464e-b4a1-3aac7c2a0025.jpeg" alt="Sorry Image">
    
    <div class="button-container" id="buttonContainer">
        <button class="choice-button yes-button" onclick="forgiveMe()">Yes</button>
        <button class="choice-button no-button" onclick="askAgain()">No</button>
    </div>

    <!-- Background Music (YouTube Autoplay) -->
    <iframe width="0" height="0" 
        src="https://www.youtube.com/embed/_HX0WvEaqks?autoplay=1&loop=1" 
        frameborder="0" allow="autoplay">
    </iframe>

    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.3.0"></script>
    <script>
        let attempts = 0; // Counter for "No" clicks

        function forgiveMe() {
            document.body.style.backgroundColor = "#ffccff"; // Change background
            document.body.innerHTML = "❤️❤️ SORRY ACCEPTED ❤️❤️"; // Change text
            confetti(); // Confetti effect
        }

        function askAgain() {
            attempts++;
            let message = document.getElementById("message");
            let buttons = document.getElementById("buttonContainer");

            if (attempts === 1) {
                message.innerHTML = "Are you sure? 🥺";
            } else if (attempts === 2) {
                message.innerHTML = "Think again... 😊";
                buttons.innerHTML = `
                    <button class="choice-button yes-button" onclick="forgiveMe()">Yes</button>
                    <button class="choice-button yes-button" onclick="forgiveMe()">Yes</button>
                `;
            }
        }
    </script>

</body>
</html>
