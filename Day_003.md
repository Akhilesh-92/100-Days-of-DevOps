# Day 3: Secure Root SSH Access

Your task is to disable direct SSH root login on all app servers within the Stratos Datacenter.

## Solution
SSH to app server 1 and modify the settings on /etc/ssh/sshd_config
```sh
ssh tony@173.21.3.20
sudo vi /etc/ssh/sshd_config
```
> change to "PermitRootLogin no"

Restart sshd service
```sh
sudo systemctl restart sshd
```

Verify SSH root login wth below command
```sh
ssh root@<app-server-ip> 
```
Repeat the above procedure on all the app servers.
