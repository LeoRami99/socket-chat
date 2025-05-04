# Back Chat - Messaging System for Hackathon Global Stablecoin Hackathon Build On Minipay With Mento Local Stablecoins

Real-time messaging system with WebSockets, Express, TypeScript, and MongoDB.

## Main Features

-   WebSockets for instant communication
-   MongoDB storage
-   RESTful API
-   Basic authentication

## Quick Setup

1. **Clone and configure:**

    ```bash
    git clone https://github.com/LeoRami99/socket-chat back-chat-hack
    cd back-chat-hack
    npm install
    ```

2. **Environment variables:**
   Create `.env` in the root:

    ```
    PORT=3000
    MONGODB_URI=mongodb://localhost:27017/chat_app
    ```

3. **Execution:**
    ```bash
    npm run dev
    ```

## Structure

```
src/
├── models/        # MongoDB Models
├── controllers/   # API Endpoints
├── services/      # Business Logic
├── sockets/       # WebSocket Management
└── config/        # Configurations
```

## Basic Usage

```javascript
// Client
const socket = io("http://localhost:3000");
socket.emit("sendMessage", { to: "user123", content: "Hello!" });
socket.on("newMessage", (msg) => console.log(msg));
```
