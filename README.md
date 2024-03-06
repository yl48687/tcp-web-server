# TCP Web Server

## Objectives
The primary objective of this project is to implement a web server using socket programming in Python. The focus is on mastering the creation of sockets, binding them to specific addresses and ports, and understanding HTTP header structure and parsing techniques. Additionally, the project aims to develop proficiency in building a web server capable of handling HTTP requests, retrieving files from the server's file system, and providing appropriate HTTP responses.

## Functionality
The server program initiates a TCP socket and binds it to a designated address and port. Upon receiving an HTTP request from a client, the server parses the request to identify the requested file. It then retrieves the file from the server's file system and constructs an HTTP response message with header lines followed by the requested file's content. This response message is transmitted directly to the client. In cases where the requested file is not found, the server sends an HTTP "404 Not Found" message to the client. Users interact with the server by sending HTTP requests and receiving responses. The server's functionality enables users to request HTML files, which the server retrieves and transmits accordingly. This project provides practical experience in implementing and interacting with web servers in Python, facilitating further exploration in web development.
