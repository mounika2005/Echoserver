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
#SERVER:
```
import socket
HOST, PORT = '127.0.0.1',65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
            

```
#CLIENT:
```
import socket
HOST, PORT = '127.0.0.1',65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'mounika, 212223100026')
    print(f'Received: {s.recv(1024)!r}')
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/6b597819-4cab-4567-94df-2e3eebb1387e)

![image](https://github.com/user-attachments/assets/07176f36-5199-43bc-bb16-9f5a1c895218)


## RESULT:
The program is executed successfully
