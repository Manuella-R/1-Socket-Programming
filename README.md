# Java Client-Server Communication Program

This project demonstrates a simple **client-server communication** system using **Java Sockets**.  
The client and server exchange messages over a socket connection until either side types `bye`, which terminates the connection.

---

## 📂 Project Structure

## ⚙️ Requirements
- **Java Development Kit (JDK)** installed (Java 8 or later).
- A terminal or command prompt.

Check if Java is installed:
```bash
java -version
javac -version
````

---

## 🚀 How to Run

### Step 1: Compile the Code

Open a terminal and navigate to the **server** directory:

```bash
cd ClientServerApp/server
javac MyServer.java
```

Then open another terminal and navigate to the **client** directory:

```bash
cd ClientServerApp/client
javac MyClient.java
```

---

### Step 2: Run the Server

In the **server** terminal:

```bash
java MyServer
```

Output:

```
Server Initiated, Waiting for Client to Connect...
```

---

### Step 3: Run the Client

In the **client** terminal:

```bash
java MyClient
```

Output:

```
Connected to Server, Please type your message and hit Enter to send
```

---

### Step 4: Start Communication

* On the **client terminal**, type a message (e.g., `Hello Server`).
* The server will receive and display the message.
* The server can then reply, and the client will see the response.

Example:

```
Client: Hello Server
Server: Hello Client
```

---

### Step 5: Terminate the Connection

Type `bye` on either client or server to close the connection.
Both terminals will show:

```
Connection Terminated
```

---

## 📝 Explanation

### MyClient.java

* Connects to server at `127.0.0.1:5555`.
* Reads input from the user and sends it to the server.
* Receives server messages and displays them.
* Terminates when either side types `bye`.

### MyServer.java

* Listens for client connections on port `5555`.
* Accepts a client socket and establishes a connection.
* Receives client messages and responds.
* Terminates when either side types `bye`.

---

## 🎯 Purpose of the Experiment

This project demonstrates how to:

1. Develop a distributed application using **Java Sockets**.
2. Understand client-server communication models.
3. Exchange messages between processes over a network.
4. Handle connection termination safely.

---

## 📌 Notes

* Both client and server must use the **same port number** (`5555`).
* `127.0.0.1` (localhost) ensures communication happens on the same machine.
* To allow connections over a network, replace `127.0.0.1` with the server's IP address.

```
