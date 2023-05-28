# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

# DATE :26-04-2023

# AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.


# ALGORITHM :

1.Import the necessary modules in python

2.Create a socket connection to using the socket module.

3.Send message to the client and receive the message from the client using the Socket module in server.

4.Send and receive the message using the send function in socket.

# PROGRAM :

## CLIENT :
```
# Developed by:SHARANGINI T K
# Register No: 212222230143
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER :
```
# Developed by:SHARANGINI TK
# Register No: 212222230143
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```

# OUTPUT :

## CLIENT :

![image](https://github.com/shara56/EX-8/assets/113497104/253b876f-3e25-4977-9c7d-359472a46068)

## SERVER :

![image](https://github.com/shara56/EX-8/assets/113497104/682d1a75-9f54-4e3b-a890-e94d019358ee)

# RESULT :

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
