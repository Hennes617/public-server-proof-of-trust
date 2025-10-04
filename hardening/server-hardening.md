
# Server Hardening Guide

## 1. Update and Upgrade
sudo apt update && sudo apt upgrade -y

## 2. SSH Setup
sudo nano /etc/ssh/sshd_config
- PermitRootLogin no
- PasswordAuthentication no
- Change Port to a custom value (z.B. 2222)
- Use only SSH keys for login
sudo systemctl restart ssh

## 3. Firewall Setup
sudo ufw default deny incoming 
sudo ufw default allow outgoing 
sudo ufw allow 2222/tcp sudo ufw enable

## 5. Disable Unnecessary Stuff
systemctl list-unit-files --type=service 
sudo systemctl disable [service-name]

## 6. Regular Security checks
- Use tools like Lynis oder rkhunter
sudo apt install lynis 
sudo lynis audit system



