# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
~~~
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break
~~~
## OUTPUT
![Client](https://github.com/hemreddy2005/2a_Stop_and_Wait_Protocol/assets/145633111/b3f7fc04-9ce8-4cd4-bd2e-c48f236a20c3)
![Server](https://github.com/hemreddy2005/2a_Stop_and_Wait_Protocol/assets/145633111/db3d3468-6fff-4fa2-908b-b4b75ffa4b5d)
## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
