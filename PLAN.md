# centralized-fss
A centralized file sharing system, built using python

### Welcome to Centralized File Sharing System

We will essentially design client and server side codes for a centralized file sharing system. The system will have a server that keeps track of the files shared by the users and the users can download the files shared by other users. The server will also keep track of the users who are online and offline. The server will also keep track of the files shared by the users and the users can download the files shared b

#### What does client do?
This can be java or python based. The client will have the following functionalities:
we dont need to implement the GUI. We can just use the command line interface.
1. Connect to the server
2. Register with the server
3. Authenticate with the server
4. Send a query to the server to search for a file
    Piggybacking: The client can send a query to the server to search for a file. The server will send the list of files that match the query. The client can then request the server to download the file.
5. Download a file from the server
6. See if any pending requests are there
7. Send a request to the server to download a file
8. Send a request to the server to upload a file

#### What does server do?
This will be a flask based server. The server will have the following functionalities:
This will be accessible through a web browser, over internet. Thus we need to maintain the security of the server.
1. Accept connections from the client
2. Accept registration requests from the client
3. Accept authentication requests from the client
4. Accept search requests from the client
5. Accept download requests from the client
6. Accept upload requests from the client
7. Accept requests from the client to see pending requests
8. Accept requests from the client to download a file
9. Accept requests from the client to upload a file
10. Keep track of the files shared by the users
11. Keep track of the users who are online and offline
12. Keep track of the pending requests
13. Provide a gui to see the files shared by the users
14. Provide a gui to see the users who are online and offline
15. Provide a gui to see the pending requests
16. Provide a gui to see the files shared by the users
17. Provide a gui to see the users who are online and offline
18. Provide a gui to see the pending requests

The Gui codes can be written in python or java. Essentially we need to have a web based gui. We can use flask for this purpose.

For the connection between the client and the server, we can use sockets. We can use the socket library in python for this purpose.
However for better performance, we can use the zeromq library. This is a high performance library for socket programming.
The starter code for zeromq looks like this:
```python
import zmq
context = zmq.Context()
socket = context.socket(zmq.REP)
socket.bind("tcp://*:5555")
```

### How will we build the system?
We will build the system in the levels. We will first build the client and server codes for the first level. Then we will build the client and server codes for the second level and so on. We will also build the gui for each level. We will also build the test cases for each level.

Each level will support a set of functionalities. We will build the client and server codes for each level. We will also build the gui for each level. We will also build the test cases for each level.

#### What are the levels?
The levels are as follows:

Level 1 The MVP, this will help us verify if the sockets work on our network.
We will support the following functionalities:
1. Connect to the server
2. Register with the server
3. Authenticate with the server
4. Send a query to the server to search for a file
5. Get a list of files that match the query

Level 2 This will help us verify if the server can keep track of the files shared by the users.
We will support the following functionalities:
All the functionalities of level 1
1. Send a request to the server to download a file
2. Send a request to the server to upload a file
3. Keep track of the files shared by the users

Level 3 This will help us verify if the server can keep track of the users who are online and offline.
We will support the following functionalities:
All the functionalities of level 2
1. Keep track of the users who are online and offline

Level 4 This will help us verify if the server can keep track of the pending requests.
We will support the following functionalities:
All the functionalities of level 3
1. Send a request to the server to see pending requests
2. Keep track of the pending requests

Hopefully this will help us build the system in a modular way. We will also build the gui for each level. We will also build the test cases for each level.

Time line:
We will build the system in the following time line:
1. Level 1: 1 week
2. Level 2: 1 week
3. Level 3: 1 week
4. Level 4: 1 week

