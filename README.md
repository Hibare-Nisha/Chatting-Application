# Java Swing Chat Application (Client-Server)

A desktop-based Client-Server Chat Application built using Java, Swing, and socket programming.
This project demonstrates core Java networking concepts (TCP sockets), multithreading and simple GUI using Swing and AWT.

## Introduction

This chat application is a simple, educational client-server program implemented in core Java. The server listens for incoming client connections and relays messages between connected parties. The client provides a Swing-based GUI for sending and receiving messages.

The project is ideal for beginners wanting to learn:
- Socket programming (java.net)
- Stream I/O (java.io)
- Multi-threading to handle multiple connections
- Basic GUI development with Swing and AWT

## Features

- Real-time text chat (TCP)
- Server waits for client connections
- Simple Swing-based GUI for client and server
- Uses core Java (no external libs)
- Easy to understand and modify

## Project Structure (suggested)

```
Java-Chat-Application/
│── README.md
│── .gitignore
│
└── src/
    ├── server/
    │   ├── Server.java
    │   └── ServerHandler.java    # optional: thread per client
    └── client/
        ├── Client.java
        └── ClientHandler.java    # optional: client-side helpers

screenshots/    # add UI screenshots
docs/           # architecture diagrams and flowcharts
```

Place your existing `src/chatting/Application/Client.java` and `src/chatting/Application/Server.java` files under the structure above or keep the current layout — the important part is that the `src` folder contains your Java sources.

## How to Run

1. Make sure you have Java JDK 8 or later installed.
2. Start the Server first:

```powershell
javac -d bin src/chatting/Application/Server.java
java -cp bin chatting.Application.Server
```

3. Start the Client (on the same machine or another machine that can reach the server):

```powershell
javac -d bin src/chatting/Application/Client.java
java -cp bin chatting.Application.Client
```

Important: start the server before starting any clients.

Note: Adjust classpaths and package names if you move files into the suggested `server`/`client` package layout.

## Requirements

- Java JDK 8 or higher
- Any OS with Java support (Windows / Linux / macOS)
- Basic knowledge of Java and socket programming

## How it Works (brief)

- The server binds to a port and listens for connections.
- A client opens a socket to the server (hostname + port).
- Server and client exchange messages over input/output streams.
- Server can spawn a new thread to handle each connected client (extendable to support many clients).

## Future Enhancements

Ideas to extend the project:

- Multi-client chat rooms / broadcasting messages to all clients
- File transfer between users
- Username authentication and active user list
- Message timestamps and message persistence (save chat history)
- Message encryption (TLS/SSL or application-level crypto)
- Voice & video chat (requires new media stack)

