# Linux CentOS7

#### Terminal Mode
``` 
su 
systemctl set-default multi-user.target 
``` 

#### Graphic Mode
``` 
su
systemctl set-default graphical.target 
```

---

OS version  
``` cat /etc/redhat-release ```  
  
Disk  
``` df -h ```  

Memory  
``` free -mt ```

Gateway  
```route -n```

Ping  
```ping -c 3 8.8.8.8 ```

SSH (Putty, Xshell, etc...)   
```
yum install -y openssh
yum install -y firewalld
systemctl start firewalld
firewall-cmd --add-port=21/tcp
firewall-cmd --reload
```



#### web console (cockpit)  
```
yum install -y cockpit
systemctl enable --now cookpit.socket
firewall-cmd --add-port=9090/tcp
firewall-cmd --add-service=cockpit
${IP Address}:9090
```
