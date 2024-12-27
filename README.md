# Java Socket Communication

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Sockets](https://img.shields.io/badge/Sockets-Networking-blue?style=for-the-badge)

A comprehensive implementation of client-server communication using Java Sockets. This project demonstrates bidirectional communication between a client and a server over TCP, showcasing fundamental concepts of networking in Java.

---

## Features

- **Full-Duplex Communication**: Enables simultaneous two-way communication between client and server.
- **Robust Error Handling**: Handles common socket communication issues gracefully.
- **Modular Code Structure**: Easy to understand, extend, and maintain.
- **Configurable Settings**: Modify host, port, and buffer sizes to suit different environments.
- **Multi-Client Support**: A scalable server implementation (if applicable).

---

## Table of Contents

- [Getting Started](#getting-started)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [How It Works](#how-it-works)
- [Customization](#customization)
- [Example Outputs](#example-outputs)
- [Contributing](#contributing)
- [License](#license)

---

## Getting Started

### Prerequisites

Ensure you have the following installed on your system:

- [Java JDK 8+](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Git](https://git-scm.com/)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/java-socket-communication.git
   ```

2. Navigate to the project directory:

   ```bash
   cd java-socket-communication
   ```

3. Compile the Java files:

   ```bash
   javac src/**/*.java
   ```

4. Run the server:

   ```bash
   java src/server/Server
   ```

5. Run the client:

   ```bash
   java src/client/Client
   ```

---

## Usage

1. Start the server by executing the server application. The server will listen on a predefined port.
2. Launch the client application and connect it to the server using the server's IP address and port.
3. Exchange messages between the client and server through the console.

---

## Code Structure

```plaintext
java-socket-communication/
├── src/
│   ├── server/
│   │   ├── Server.java
│   │   └── ServerHandler.java
│   ├── client/
│   │   ├── Client.java
│   │   └── ClientHandler.java
├── README.md
└── LICENSE
```

- **Server.java**: Entry point for the server-side application.
- **Client.java**: Entry point for the client-side application.
- **Handler Classes**: Handle individual client connections and communication.

---

## How It Works

1. **Server Initialization**:
   - The server binds to a specified port and listens for incoming client connections.
   - For every client connection, a new thread is spawned to handle communication.

2. **Client Connection**:
   - The client establishes a socket connection with the server.
   - Messages are sent and received using input and output streams.

3. **Communication**:
   - Both client and server exchange messages over TCP in real time.

---

## Customization

- **Change Host and Port**:
  Modify the host and port in `Server.java` and `Client.java`:
  
  ```java
  String host = "127.0.0.1"; // Default localhost
  int port = 8080;           // Default port
  ```

- **Add Multi-Client Support**:
  Extend the server to handle multiple clients by managing threads for each connection.

---

## Example Outputs

### Server
```plaintext
Server started on port 8080.
Client connected: 127.0.0.1
Message from client: Hello, Server!
Message sent to client: Hello, Client!
```

### Client
```plaintext
Connected to server at 127.0.0.1:8080
Message sent to server: Hello, Server!
Message from server: Hello, Client!
```

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeatureName`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeatureName`).
5. Open a Pull Request.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
