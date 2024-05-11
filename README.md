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
### client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())  

```

### server:
```
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```

## OUPUT
### client:
![315944467-6956748a-e213-43ca-8ebf-b2226671c352](https://github.com/A-Thiyagarajan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/118707693/1295284d-c30f-4ca6-9a16-404e6f78bedb)

### server:
![315944522-31f44652-370b-48f5-9712-f2e2c65ac203](https://github.com/A-Thiyagarajan/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/118707693/a55a20de-d10a-44b5-8211-d463fb79fca4)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
