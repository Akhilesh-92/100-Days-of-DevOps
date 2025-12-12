# Day 3: Secure Root SSH Access

Your task is to disable direct SSH root login on all app servers within the Stratos Datacenter.

## Solution
```sh
ssh tony@173.21.3.20
sudo vi /etc/ssh/sshd_config, change to "PermitRootLogin no"
sudo systemctl restart sshd
Verify ssh root@<app-server-ip> 
```
