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

## Server
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

## Client

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUPUT

## server
<img width="641" height="182" alt="Screenshot 2025-09-19 112936" src="https://github.com/user-attachments/assets/f41a39ef-ac82-4b0d-9297-f77b7c6fb57d" />

## Client
<img width="560" height="181" alt="Screenshot 2025-09-19 112953" src="https://github.com/user-attachments/assets/3cc85bb9-b3fa-4858-a59c-e5b12fee4567" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
