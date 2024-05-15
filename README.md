# EXP: 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM:
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
### Client:
```py
import socket
s = socket.socket()
s.connect(('localhost',8000))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())
```
### Server:
```py
import socket
s = socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c, addr = s.accept()
while True:
    ClientMessage = c.recv(1024).decode()
    print("Client > ", ClientMessage)
    msg = input("Server > ")
    c.send(msg.encode())
 ```
## OUPUT:
### Client:
<img width="439" alt="324196662-bc5da1e0-aaeb-4ebc-9517-a1c5c741e68e" src="https://github.com/kanishka2305/3b_CHAT_USING_TCP_SOCKETS/assets/113497357/4f277f1f-3c23-40cb-87b7-e4a4a9897532">
### Server
<img width="438" alt="324196686-9a4ac5ed-2f70-4a01-88c2-0dcfd9d3736e" src="https://github.com/kanishka2305/3b_CHAT_USING_TCP_SOCKETS/assets/113497357/4b324aac-9d99-4526-a07b-acef0fa1e857">

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
