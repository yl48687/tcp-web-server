# TCP Web Server
The project develops a web server capable of handling one HTTP request at a time. The server should accept and parse the HTTP request, retrieve the requested file from the server's file system, construct an HTTP response message with appropriate header lines, and send the response directly to the client. If the requested file is not found, the server should respond with an "HTTP 404 Not Found" message.

## Design Overview
The project is designed to handle HTTP requests sequentially using Python. It employs TCP sockets for communication.

## Functionality
`server.py`:
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
