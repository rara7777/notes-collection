<a name="#Linux"></a>
# 在Ubuntu上設定並部署Laravel程式

## 開始之前

### 設定時區為 Asia/Taipei
```
sudo timedatectl set-timezone Asia/Taipei
```

### 建立使用者(已有root以外使用者可略過)
建立其他使用者以避免使用root登入以提升安全性
```
adduser yourUserNameHere
```
令該使用者擁有sudo權限
```
adduser yourUserNameHere sudo
```

### 關閉root登入
```
nano etc/ssh/ssshd/config
```
修改 PermitRootLogin 為 no，並重載ssh服務
```
systemtcl reload ssh.service
```

## 設定Apache
### Install Apache
```
sudo apt update
sudo apt install apache2
```

確認是否可以瀏覽
```
http://your_server_ip
```

### 設定網站
```
cd /etc/apache2/sites-available
sudo cp default yourdomain.com
sudo nano yourdomain.com
```

Modify settings
```
root /var/www/html; -> root /var/www/yourdomain.com

serverName _; -> server_name yourdomain.com;
```

重啟服務
```
sudo systemctl reload apache2.service
```
或
```
sudo service apache2 restart
```

## Setting up database
安裝資料庫，此用mysql，亦可改安裝mariadb
```
sudo apt update
sudo apt install mysql-server
sudo mysql_secure_installation
-> Setting root pasword? [Y/n] Y
-> Remove anonymous users? [Y/n] Y
-> Disallow root login remotely? [Y/n] Y
-> Removetest database and access to it? [Y/n] Y
-> Reload privilege tables noew? [Y/n] Y
```

建立一個資料庫使用者
```
sudo mysql -u root -p
create user yourdomain.com@% identified by 'yourpassword';
create database yourdomain.com;
grant all privileges on yourdomain.com.* to yourdomain.com@%;
flush privileges;
```

## 設定PHP
### 安裝 PHP 7.4
```
sudo apt update
sudo apt upgrade
sudo apt install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php7.4
```

確認是否安裝成功
```
php -v
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

## Laravel Permissions
```
chown -R thingstech storage/
chown -R thingstech bootstrap/
```

## References
- [Initial Server Setup with Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/initial-server-setup-with-ubuntu-18-04)
- [How To Install Linux, Apache, MySQL, PHP (LAMP) stack on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-ubuntu-18-04)
- [Install PHP 7.4 on Ubuntu 18.04](https://www.cloudbooklet.com/install-php-7-4-on-ubuntu)
- [Upgrade PHP version to PHP 7.4 on Ubuntu](https://www.cloudbooklet.com/upgrade-php-version-to-php-7-4-on-ubuntu/)

