# EX.NO:3b.           CREATION FOR CHAT USING TCP SOCKETS

## AIM:
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python</br>
2. Create a socket connection to using the socket module.</br>
3. Send message to the client and receive the message from the client using the Socket module in
 server</br>
4. Send and receive the message using the send function in socket.</br>

## PROGRAM:
### Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server
```
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
```
## OUTPUT:
### Client
![image](https://github.com/Yuvaranithulasingam/3b_CHAT_USING_TCP_SOCKETS/assets/121418522/1c832b11-ad68-48f3-a4d1-2a0314b9b63a)
### Server
![image](https://github.com/Yuvaranithulasingam/3b_CHAT_USING_TCP_SOCKETS/assets/121418522/b1351a91-1d5c-46b0-8b5f-f276ebceb11d)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
