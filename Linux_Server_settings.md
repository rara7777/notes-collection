<a name="#Linux"></a>
# Simple Linux server settings

## create users
create a new user
```
adduser: adduser yourUserNameHere
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
