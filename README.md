<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>QuizEnglish AI</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #343541;
      color: #ececf1;
      display: flex;
      height: 100vh;
    }
    .sidebar {
      width: 250px;
      background-color: #202123;
      padding: 20px;
      box-sizing: border-box;
    }
    .sidebar h2 {
      font-size: 18px;
      margin-bottom: 10px;
    }
    .sidebar ul {
      list-style: none;
      padding: 0;
    }
    .sidebar ul li {
      padding: 10px;
      background-color: #2f3035;
      margin-bottom: 5px;
      cursor: pointer;
      border-radius: 6px;
    }
    .chat-container {
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      padding: 20px;
    }
    .chat-box {
      flex-grow: 1;
      overflow-y: auto;
      margin-bottom: 10px;
    }
    .chat-input {
      display: flex;
    }
    .chat-input input {
      flex-grow: 1;
      padding: 10px;
      border: none;
      border-radius: 6px;
      font-size: 16px;
    }
    .chat-input button {
      padding: 10px 20px;
      margin-left: 10px;
      background-color: #10a37f;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }
    .message {
      background-color: #444654;
      padding: 10px;
      border-radius: 6px;
      margin-bottom: 10px;
    }
  </style>
</head>
<body>
  <div class="sidebar">
    <h2>📚 QuizEnglish AI</h2>
    <ul>
      <li>New Chat</li>
      <li>Grammar Tips</li>
      <li>IELTS Practice</li>
      <li>Speaking Guide</li>
      <li>Contact</li>
    </ul>
  </div>
  <div class="chat-container">
    <div class="chat-box" id="chat-box">
      <div class="message">👋 Hello! I am your English learning assistant. Ask me anything!</div>
    </div>
    <div class="chat-input">
      <input type="text" id="user-input" placeholder="Type your question..." />
      <button onclick="sendMessage()">Send</button>
    </div>
  </div>

  <script>
    function sendMessage() {
      const input = document.getElementById("user-input");
      const chatBox = document.getElementById("chat-box");
      const userMessage = input.value.trim();
      if (userMessage === "") return;
      const userDiv = document.createElement("div");
      userDiv.className = "message";
      userDiv.textContent = "You: " + userMessage;
      chatBox.appendChild(userDiv);
      input.value = "";
      const botDiv = document.createElement("div");
      botDiv.className = "message";
      botDiv.textContent = "QuizEnglish AI: I'm still learning, but I'm here to help you study!";
      chatBox.appendChild(botDiv);
      chatBox.scrollTop = chatBox.scrollHeight;
    }
  </script>
</body>
</html>
