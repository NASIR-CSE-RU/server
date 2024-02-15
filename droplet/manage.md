## Enable password authentication in digitalocean droplet

1. Log as as a root to you Ubuntu server

```  

vim /etc/ssh/sshd_config

 ```

2. Now go to very bottom and change the value from "no" to "yes".

It should look like this:

Change to no to disable tunnelled clear text passwords
```shell
PasswordAuthentication yes
service sshd reload
```
3. Now you can access your vps by using password
```shell
ssh root@server_ip_or_domain
```


## restart nextjs project in nginx server with pm2

1. Go to /var/www/second-app and open package.json file with vim.
```shell
cd /var/www/second-app
vim package.json
```
2. Now you can see the project name
```json
{
  "name": "second-app",
  "version": "0.1.0",
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start -p 3001" # !!! This time, we use port 3001
  },
  "dependencies": {
    "next": "latest",
    "react": "latest",
    "react-dom": "latest"
  }
}
```
3. Rebuild the app and start it with PM2.
```shell
npm run build
pm2 start npm --name "second-app" -- start
```
4. We can check pm2 status with pm2 status command.
```shell
pm2 status
```