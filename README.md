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
~~~
CLIENT:
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
~~~
~~~
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
~~~
## OUTPUT
CLIENT
<img width="1470" height="195" alt="442404555-88f83eba-861d-483f-b858-b8e55a135104" src="https://github.com/user-attachments/assets/da08478c-7088-472d-a3ea-7ba624b28e9d" />

SERVER
<img width="1576" height="240" alt="442404572-d331586f-dc6d-4b1a-a01e-999b6cfe3873" src="https://github.com/user-attachments/assets/01547691-73cb-4b02-b4b9-926d9bd3e3b2" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
