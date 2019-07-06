<a name="#Linux"></a>
# Simple Linux server settings

## Setting up timezone
```
timedatectl set-timezone Asia/Taipei
```

## create users
create a new user
```
adduser yourUserNameHere
```
make the user has permission to sudo
```
adduser yourUserNameHere sudo
```

if you want to del user
```
deluser yourUserNameHere
```

## preventing root login
1. nano etc/ssh/ssshd/config
2. change PermitRootLogin to no
3. systemtcl reload ssh.service

## UFW firewall


## Permissions
chown -R thingstech storage/
chown -R thingstech bootstrap/

## fail2ban
```
sudo apt-get update
sudo apt install fail2ban
```

## Nginx
### Install Nginx
```
sudo apt update
sudo apt install nginx
```

### Allowing access
```
sudo ufw status verbose
sudo ufw app list
sudo ufw allow "Nginx Full"
```

Important files located in /etc/nginx/

### Setting up sites
```
cd /etc/nginx/sites-available
sudo cp default yourdomain.com
sudo nano yourdomain.com
```

Modify settings
```
root /var/www/html; -> root /var/www/yourdomain.com

server_name _; -> server_name yourdomain.com;
```

Restart service
```
sudo ln -s /etc/nginx/sites-available/yourdomain.com /etc/nginx/sites-enabled/yourdomain.com
sudo systemctl reload nginx.service
```

## Setting up database
Install Database
```
sudo apt update
sudo apt install mariadb-server
sudo mysql_secure_installation
-> Setting root pasword? [Y/n] Y
-> Remove anonymous users? [Y/n] Y
-> Disallow root login remotely? [Y/n] Y
-> Removetest database and access to it? [Y/n] Y
-> Reload privilege tables noew? [Y/n] Y
```

Create users for projects
```
sudo mysql -u root -p
create user yourdomain.com@% identified by 'yourpassword';
create database yourdomain.com;
grant all privileges on yourdomain.com.* to yourdomain.com@%;
flush privileges;
```

## Setting up PHP
```
sudo apt-get update
sudo apt install php-fpm
```




