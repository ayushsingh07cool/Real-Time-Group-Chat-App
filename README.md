💬 Real-Time Chat Application (Spring Boot + WebSocket + STOMP)

A simple real-time chat application built using Spring Boot, WebSocket, and STOMP protocol.
It allows multiple users to send and receive messages instantly using a publish/subscribe messaging model.

🚀 Features

✅ Real-time messaging using WebSockets
✅ STOMP protocol for structured message routing
✅ Broadcast messages to all connected users
✅ SockJS fallback for browsers that don’t support native WebSockets
✅ Lightweight frontend using HTML + JavaScript
✅ Configurable CORS and server port


| Layer      | Technology                                              |
| ---------- | ------------------------------------------------------- |
| Backend    | Spring Boot, Spring WebSocket, Spring Messaging (STOMP) |
| Frontend   | HTML, JavaScript, SockJS, Stomp.js                      |
| Build Tool | Maven                                                   |
| Language   | Java 17+                                                |


Project Structure 
src/main/java/com/chat/app
│
├── config/
│   └── WebSocketConfig.java          # WebSocket + STOMP configuration
│
├── controller/
│   └── ChatController.java           # Handles messages from clients
│
├── model/
│   └── ChatMessage.java              # Represents chat message structure
│
├── AppApplication.java               # Main Spring Boot application class
│
└── resources/
    ├── static/
    │   └── chat.html                 # Frontend chat page
    └── application.properties        # Server configuration



⚡ How It Works

Client connects to the endpoint /chat using SockJS.

Client sends messages to /app/sendmessage.

The message is handled in ChatController

All subscribed clients receive the message from /topic/messages.



   
