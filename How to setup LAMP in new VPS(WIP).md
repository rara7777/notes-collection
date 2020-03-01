<a name="#Linux"></a>
# How to setup LAMP in new VPS

## Before Start

### Setting up timezone
```
sudo timedatectl set-timezone Asia/Taipei
```

### create users
create a new user to login instead of root login
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

### preventing root login
```
nano etc/ssh/ssshd/config
```
change PermitRootLogin to no
```
systemtcl reload ssh.service
```

## UFW firewall

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
### Install PHP
```
sudo apt-get update
sudo apt install php-fpm
```

### Securing PHP
```
sudo nano /etc/php/7.2/fpm/php.ini
```
cgi.fix_pathinfo=1 -> cgi.fix_pathinfo=0
### Sending requests from nginx to php-fpm
```
sudo nano /etc/nginx/sites-available/yourdomain.com
```

modify
```
index index.php index.html

...

location ~ \.php# {
    include snippets/fastcgi-php.conf;
    fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
}
```

reload sevice
```
sudo systemctl reload nginx.service
```

## Making more safe
### 1.  prevent access to .htaccess and .git files
```
location ~ /\.ht {
    deny all;
}
location ~ /\.git {
    deny all;
}
```

### 2. Hiding the Nginx signature in the responses
```sudo nano /etc/nginx/nginx.conf```

## Laravel Permissions
```
chown -R thingstech storage/
chown -R thingstech bootstrap/
```

## References
- [Initial Server Setup with Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04)
- [How To Install Linux, Apache, MySQL, PHP (LAMP) stack on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-ubuntu-18-04)
