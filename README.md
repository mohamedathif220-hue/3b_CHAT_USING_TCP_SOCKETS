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
server.py
```
server.py
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
client.py
```
client.py
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
<img width="1047" height="181" alt="Screenshot 2026-03-19 154833" src="https://github.com/user-attachments/assets/26c66160-087a-4655-90eb-7a0bddacf766" />
<img width="1043" height="193" alt="Screenshot 2026-03-19 154845" src="https://github.com/user-attachments/assets/289b46e8-e557-427a-a6ce-cf9ec4b5114d" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
