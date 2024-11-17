# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name:Sandeep S
## Reg:212223220092
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

# CLIENT: 
 ```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
# SERVER:
```
SERVER: 
 
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

## OUPUT
# CLIENT
![image](https://github.com/user-attachments/assets/2e99bd00-6b22-4857-8779-5618ad185ecd)

# SERVER
![image](https://github.com/user-attachments/assets/f03462f6-e80b-440d-a57b-19a1ca9a4c9d)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
