# 💬 Chat Application — Real-Time Messaging System

A real-time chat application built with **Spring Boot** and **WebSocket**, enabling users to send and receive messages instantly without any page refresh.

---

## 🚀 Features

- ⚡ **Real-Time Messaging** — Instant message delivery using WebSocket
- 📡 **Live Broadcasting** — Messages broadcast to all connected users simultaneously
- 🔄 **Bidirectional Communication** — Full-duplex communication using STOMP over WebSocket
- 🖥️ **Responsive UI** — Clean and dynamic interface built with Thymeleaf and Bootstrap
- 🚫 **No Page Refresh** — Seamless chat experience with JavaScript handling updates

---

## 🛠️ Tech Stack

| Layer       | Technology                        |
|-------------|-----------------------------------|
| Language    | Java 17                           |
| Framework   | Spring Boot                       |
| Messaging   | Spring WebSocket + STOMP Protocol |
| Frontend    | Thymeleaf, JavaScript, Bootstrap  |
| Build Tool  | Maven                             |

---

## 📁 Project Structure

```
chatApplication/
├── src/
│   └── main/
│       ├── java/com/chat/application/
│       │   ├── config/         # WebSocket configuration
│       │   ├── controller/     # ChatController (message handling)
│       │   └── model/          # ChatMessage model
│       └── resources/
│           ├── templates/      # Thymeleaf HTML templates
│           └── application.properties
├── pom.xml
└── README.md
```

---

## ⚙️ Getting Started

### Prerequisites

- Java 17+
- Maven 3.8+

### 1. Clone the repository

```bash
git clone https://github.com/abhaypalke/chatApplication.git
cd chatApplication
```

### 2. Run the application

```bash
./mvnw spring-boot:run
```

The server will start at **http://localhost:8080**

### 3. Open in browser

```
http://localhost:8080
```

Open the same URL in **multiple browser tabs** to test real-time messaging between users!

---

## 💡 How It Works

1. User opens the chat page in the browser
2. A **WebSocket connection** is established with the server
3. When a user sends a message, it goes to the Spring Boot backend via `@MessageMapping`
4. The server broadcasts the message to all connected clients via `@SendTo`
5. All users see the message instantly — **no page refresh needed**

---

## 📌 Key Endpoints

| Type      | Endpoint             | Description                        |
|-----------|----------------------|------------------------------------|
| HTTP GET  | `/`                  | Opens the chat UI                  |
| WebSocket | `/ws`                | WebSocket connection endpoint      |
| STOMP     | `/app/sendMessage`   | Send a message to the server       |
| STOMP     | `/topic/messages`    | Subscribe to receive all messages  |

---

## 🙋‍♂️ Author

**Abhay Palke**
- 📧 abhaypalke4@gmail.com
- 💼 [LinkedIn](https://www.linkedin.com/in/abhaypalke)
- 🐙 [GitHub](https://github.com/abhaypalke)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
