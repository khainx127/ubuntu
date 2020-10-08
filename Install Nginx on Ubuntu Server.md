To install Nginx on Ubuntu Server, run these commands:
```
sudo apt update
sudo apt install nginx
```
Enable Firewall & allow SSH:
```
sudo ufw reset
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw app list
sudo ufw allow 'Nginx Full'
sudo ufw allow 'OpenSSH'
sudo ufw enable
sudo ufw status
systemctl status nginx
```
Check status of Nginx ```systemctl status nginx```
