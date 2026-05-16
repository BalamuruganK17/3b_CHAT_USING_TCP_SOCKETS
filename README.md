# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER
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
## OUPUT:
<img width="764" height="543" alt="Screenshot 2026-05-16 125247" src="https://github.com/user-attachments/assets/838bee93-38f9-4a12-94dc-d2dfbd929abe" />
<img width="776" height="496" alt="Screenshot 2026-05-16 125259" src="https://github.com/user-attachments/assets/c49c5f30-ef38-483c-bb96-576c7e5c8df8" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
