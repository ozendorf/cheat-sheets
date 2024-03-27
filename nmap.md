## Nmap Cheat Sheet


## 1. Port Scan: Scan specific ports on a target.
```
nmap -p <port1,port2,...> <target>
```

## 2. Scan All Ports: Scan all 65535 ports on a target.
```
nmap -p- <target>
```

## 3. Service Version Detection: Detect versions of services running on open ports.
```
nmap -sV <target>
```

## 4. Operating System Detection: Attempt to determine the OS of the target.
```
nmap -O <target>
```

##  5. Aggressive Scan: Enables OS detection, version detection, script scanning, and traceroute.
```
nmap -A <target>
```



