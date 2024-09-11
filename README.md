NAME : Preethika N                 
REG NO : 212223040130

# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM  

CLIENT:

import socket     
s=socket.socket()             
s.connect(('localhost',8000))                 
while True:                   
    msg=input("Client > ")               
    s.send(msg.encode())                          
    print("Server > ",s.recv(1024).decode())                   


SERVER:

import socket      
s=socket.socket()          
s.bind(('localhost',8000))              
s.listen(5)                  
c,addr=s.accept()                 
while True:                                
    ClientMessage=c.recv(1024).decode()          
    c.send(ClientMessage.encode())               


##OUTPUT:
CLIENT :

![image](https://github.com/user-attachments/assets/277bf600-3e9d-4d86-a922-2c633b0de56d)


SERVER:

![image](https://github.com/user-attachments/assets/4c63fbb0-8be3-48a2-940d-f58a39dafad4)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
