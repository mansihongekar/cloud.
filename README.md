<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College Enquiry Chatbot</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .chat-container {
            background: #fff;
            border: 1px solid #ccc;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 400px;
            max-width: 90%;
            padding: 20px;
        }
        h1 {
            font-size: 1.5em;
            color: #333;
            text-align: center;
        }
        .chat-box {
            margin-top: 20px;
        }
        .chat-box input[type="text"] {
            width: 100%;
            padding: 10px;
            font-size: 1em;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .chat-box button {
            margin-top: 10px;
            width: 100%;
            padding: 10px;
            font-size: 1em;
            background-color: #007BFF;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .chat-box button:hover {
            background-color: #0056b3;
        }
        .response {
            margin-top: 20px;
            padding: 10px;
            background-color: #f1f1f1;
            border-radius: 5px;
            font-size: 1em;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="chat-container">
        <h1>College Enquiry Chatbot</h1>
        <div class="chat-box">
            <input type="text" id="userInput" placeholder="Ask your question...">
            <button onclick="sendMessage()">Submit</button>
        </div>
        <div id="chatResponse" class="response"></div>
    </div>

  <script>
        function sendMessage() {
            const userInput = document.getElementById('userInput').value;
            const responseDiv = document.getElementById('chatResponse');

            // Example static responses
            const responses = {
                "what is the admission process?": "The admission process involves submitting your documents and completing an online application.",
                "what courses are offered?": "We offer courses in Computer Science, Electronics, Mechanical Engineering, and Civil Engineering.",
                "what is the fee structure?": "The fee structure varies by course. Please check our website for detailed information."
            };

            const response = responses[userInput.toLowerCase()] || "Sorry, I don't have an answer to that. Please contact support.";
            responseDiv.textContent = response;

            // Clear the input field
            document.getElementById('userInput').value = '';
        }
    </script>
</body>
</html>

