# EXP : 4 - Execution_of_NetworkCommands
## AIM :
Use of Network commands in Real Time environment
## Software : 
Command Prompt And Network Protocol Analyzer
## Procedure: 
To do this EXPERIMENT- follows these steps :
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
All commands related to Network configuration which includes how to switch to privilege mode
and normal mode and how to configure router interface and how to save this configuration to
flash memory or permanent memory.
This commands includes

• Configuring the Router commands

• General Commands to configure network

• Privileged Mode commands of a router 

• Router Processes & Statistics

• IP Commands

• Other IP Commands e.g. show ip route etc.


<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>

## PROGRAM :
### PING COMMAND -
#### CLIENT 
```
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    hostname=c.recv(1024).decode()
    try:
        c.send(str(ping(hostname,verbose=False)).encode())
    except KeyError:
        c.send("Not Found".encode())
```

#### SERVER
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    ip=input("Enter the website you want to ping ")
    s.send(ip.encode())
    print(s.recv(1024).decode())
```

### TRACEROUTE COMMAND -
```
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>
<BR>

## OUTPUT :
### PING COMMAND 
![image](https://github.com/MOHAMEDAHSAN/4.Execution_of_NetworkCommends/assets/139331378/7fe8c671-8f7b-49e0-9b41-8927e3d742df)

### TRACEROUTE
![318509371-ed1e8d7d-22d4-400f-b102-fefe2c182e45](https://github.com/MOHAMEDAHSAN/4.Execution_of_NetworkCommends/assets/139331378/e5cc5174-d202-474f-b271-a6c5266c3e68)

## Result :
Thus Execution of Network commands Performed 
