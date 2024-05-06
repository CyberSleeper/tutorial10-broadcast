# Reflection

## 2.1. Original code of broadcast chat
![alt text](image.png)
To run the server, we run `cargo run --bin server`. To run the client, we run `cargo run --bin client`. We just implemented websocket communication between the server and the client. When any client sends a message, it will be broadcasted to all clients. We can run multiple clients and see the messages being broadcasted to all clients.

### 2.2. Modifying the websocket port
In terms of websocket port, we can modify the port by changing the port number in the server code. We can change the port number in the server code by changing the port number in the `Server::bind` function. We can change the port number in the client code by changing the port number in the `Client::connect` function.

If we take a look at the `server.rs`, it don't need to initiate any WebSocket connection because it is a server. It just need to bind the address and listen to the incoming connection. The WebSocket connection will be initiated by the client. The server will accept the incoming connection and handle the incoming message.