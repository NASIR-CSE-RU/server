# How to install free ssh in Cpanel
## install acme.sh
```curl https://get.acme.sh | sh```
## Generate certificate
```.acme.sh/acme.sh --issue -d poultry.devmines.com -d www.poultry.devmines.com -w /home/devmxkxq/poultry.devmines.com --server letsencrypt```
## Install ssh
  1. go to ```SSL/TLS```
  2. click  ```Manage SSL sites```.
  3. select a domain
  4. provide ```Certificate: (CRT)``` and ```Private Key (KEY)``` from ```.acme.sh/poultry.devmines.com_ecc``` folder ```poultry.devmines.com.cer``` and ```poultry.devmines.com.key``` file respectively
  5. click ```Install Certificate```
## check ssh
SSL Checker Tool: https://wphowknow.com/ssl-checker/
