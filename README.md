# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
```
Developed by: Ashqar Ahamed S.T
Register no: 212224240018

# Server Program:
import socket
Host, Port = '127.0.0.1', 65000
with socket.create_server((Host, Port)) as server:
    conn, addr = server.accept()
    print(f"connected by {addr}")

    data = conn.recv(1024)
    print(f"Received: {data.decode()}")
    
    conn.sendall(b'My name is Ashqar')

# Client Program:
import socket
Host, Port = '127.0.0.1', 65000

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as client:
    client.connect((Host, Port))
    client.sendall(b"Ashqar Ahamed S T, 212224240018")

    response = client.recv(1024)
    print(f"Server says: {response.decode()}")
```
## OUTPUT:
## Server Output
![output1](https://github.com/user-attachments/assets/8ab839ac-07af-40af-a0e2-8a0b1b01fe4e)
## Client Output
![output2](https://github.com/user-attachments/assets/8b6ed182-bc50-4b3d-9a46-054941c8471c)

## RESULT:
The program is executed successfully
