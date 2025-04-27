<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI 聊天室</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f7f6f3;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
        }

        .chat-container {
            width: 100%;
            max-width: 800px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }        .chat-header {
            background-color: #9b958f;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .chat-messages {
            height: 400px;
            overflow-y: auto;
            padding: 20px;
        }

        .message {
            margin-bottom: 15px;
            display: flex;
            align-items: flex-start;
        }

        .message.user {
            flex-direction: row-reverse;
        }

        .message-content {
            max-width: 70%;
            padding: 10px 15px;
            border-radius: 15px;
            margin: 0 10px;
        }        .user .message-content {
            background-color: #9b958f;
            color: white;
        }

        .ai .message-content {
            background-color: #e9ecef;
            color: black;
        }

        .chat-input {
            display: flex;
            padding: 20px;
            border-top: 1px solid #ddd;
        }

        #user-input {
            flex: 1;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-right: 10px;
        }        #send-button {
            padding: 10px 20px;
            background-color: #9b958f;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }        #send-button:hover {
            background-color: #827c76;
        }
    </style>
</head>
<body>    <div class="chat-container">
        <div class="chat-header">
            <h1>AI 聊天室</h1>
        </div>
        <div class="chat-messages" id="chat-messages"></div>
        <div class="chat-input">
            <input type="text" id="user-input" placeholder="輸入訊息..." autofocus>
            <button id="send-button">發送</button>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
