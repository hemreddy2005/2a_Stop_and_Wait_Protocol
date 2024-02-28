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
![Pic 1](https://github.com/hemreddy2005/2a_Stop_and_Wait_Protocol/assets/145633111/a5b1e3f5-9070-4f55-93cf-bcf264513d20)
![Pic 2](https://github.com/hemreddy2005/2a_Stop_and_Wait_Protocol/assets/145633111/cdbf6a6b-9eb9-4766-89f2-14aba1e57f84)
## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
