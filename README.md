<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rewrite Biased Prompts</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f5f5f5;
            padding: 20px;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            width: 50%;
            margin: auto;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }
        textarea {
            width: 80%;
            height: 50px;
            padding: 10px;
            font-size: 16px;
            margin-top: 10px;
        }
        button {
            margin-top: 10px;
            padding: 10px;
            font-size: 16px;
            background-color: #28a745;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #218838;
        }
        .feedback {
            margin-top: 15px;
            font-weight: bold;
            color: #333;
        }
    </style>
</head>
<body>

    <div class="container">
        <h2>Rewrite Biased Prompts</h2>
        <p><strong>Original Prompt:</strong> Why are traditional medicines ineffective compared to modern medicine?</p>
        <textarea id="userInput" placeholder="Rewrite the prompt..."></textarea>
        <br>
        <button onclick="checkPrompt()">Submit</button>
        <p class="feedback" id="feedback"></p>
    </div>

    <script>
        function checkPrompt() {
            let userPrompt = document.getElementById("userInput").value.toLowerCase();
            let feedback = document.getElementById("feedback");
            
            let optimizedPrompt = "Compare the effectiveness of traditional and modern medicine in different contexts.";

            if (userPrompt.includes("compare") && userPrompt.includes("traditional") && userPrompt.includes("modern")) {
                feedback.innerHTML = "✅ Great job! Your revised prompt is more neutral and encourages balanced discussion.";
                feedback.style.color = "green";
            } else {
                feedback.innerHTML = "❌ Try again! Consider making the prompt neutral by removing assumptions and allowing comparison.";
                feedback.style.color = "red";
            }
        }
    </script>

</body>
</html>
