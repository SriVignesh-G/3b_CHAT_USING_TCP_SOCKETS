# Ex No:3b CREATION FOR CHAT USING TCP SOCKETS
# Name: Sri Vignesh G
# Reg No: 212223040204
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client.py:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server.py:
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUTPUT:
### Client Window:
![Screenshot 2024-04-19 232002](https://github.com/SriVignesh-G/3b_CHAT_USING_TCP_SOCKETS/assets/147576510/cc5af3ef-01c2-469c-8157-4cb4370dcfef)

### Server Window:
![Screenshot 2024-04-19 232008](https://github.com/SriVignesh-G/3b_CHAT_USING_TCP_SOCKETS/assets/147576510/5aea8a4e-126f-4dae-97ce-72a4b94d73ba)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
