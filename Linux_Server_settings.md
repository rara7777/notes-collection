<a name="#Linux"></a>
# Linux server settings

## create users
adduser: adduser thingstech
adduser(has permission): adduser thingstech sudo
deluser: deluser thingstech

## preventing root login
1. nano etc/ssh/ssshd/config
2. change PermitRootLogin to no
3. systemtcl reload ssh.service

## UFW firewall


## Permissions
chown -R thingstech storage/
chown -R thingstech bootstrap/

## fail2ban
sudo apt-get update
sudo apt install fail2ban

