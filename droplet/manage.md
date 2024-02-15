## Enable password authentication in digitalocean droplet

1. Log as as a root to you Ubuntu server

```  

vim /etc/ssh/sshd_config

 ```

2. Now go to very bottom and change the value from "no" to "yes".

It should look like this:

Change to no to disable tunnelled clear text passwords
``` 

PasswordAuthentication yes
service sshd reload

```
3. Now you can access your vps by using password
```

ssh root@server_ip_or_domain

```
