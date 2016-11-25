
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





