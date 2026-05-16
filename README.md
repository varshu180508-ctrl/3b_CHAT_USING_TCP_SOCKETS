# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM

To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:

1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.


## PROGRAM

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

    
## OUPUT

CLIENT

<img width="1920" height="1056" alt="Screenshot (170)" src="https://github.com/user-attachments/assets/0a50e44f-d68d-4487-a37e-1d88bb6f44aa" />

SERVER

<img width="1920" height="829" alt="Screenshot (171)" src="https://github.com/user-attachments/assets/31a3e925-7c54-4204-93ef-88ae2acc901d" />

##RESULT

Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
