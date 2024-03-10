# TCP Web Server
The project develops a web server capable of handling one HTTP request at a time. The server should accept and parse the HTTP request, retrieve the requested file from the server's file system, construct an HTTP response message with appropriate header lines, and send the response directly to the client. If the requested file is not found, the server should respond with an "HTTP 404 Not Found" message.

## Design Overview
The project is designed to handle HTTP requests sequentially using TCP sockets in Python. The server listens for incoming connections on a specified address and port. Upon receiving a connection, it accepts and parses the HTTP request message from the client. It then extracts the requested file name from the request, reads the corresponding file from the server's file system, and constructs an HTTP response message containing the file content preceded by header lines. If the requested file is not found, the server sends an "HTTP 404 Not Found" response. Finally, the server sends the HTTP response message back to the client and closes the connection.

## Functionality
`server`:
- Listens for incoming connections from clients. Upon receiving a connection request, accepts the connection and creates a new socket for communication.
- Receives the HTTP request message from the connected client.
- Parses the HTTP request message to extract the name of the file requested by the client.
- Opens the requested file from the server's file system.
- Reads the content of the requested file.
- Sends HTTP header lines to the client indicating a successful response (HTTP 200 OK).
- Sends the content of the requested file to the client over the established connection.
- Sends an HTTP 404 Not Found response to the client if the requested file is not found in the server's file system.
- Closes the connection socket after sending the file content or the error response.
- Terminates the server program in case of errors or file not found situations

## File Structure and Content
```
tcp-web-server/
├── HelloWorld.html
├── README.md
└── server.py
```
