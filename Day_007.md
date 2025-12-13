# Day 7: Linux SSH Automation
The system admins team of xFusionCorp Industries has set up some scripts on jump host that run on regular intervals and perform operations on all app servers in Stratos Datacenter. To make these scripts work properly we need to make sure the thor user on jump host has password-less SSH access to all app servers through their respective sudo users (i.e tony for app server 1). Based on the requirements, perform the following:

Set up a password-less authentication from user thor on jump host to all app servers through their respective sudo users.

## Solution
SSH to jump host
```sh
ssh thor@<jump_host>
```
Generate a RSA key
```sh
ssh-keygen -t rsa -b 2048
```
Copy the generated key to all the app servers
```sh
ssh-copy-id <sudo_user>@<app_server_ip>
```
Verify by logging in to each server
```sh
ssh tony@172.16.238.10
ssh steve@172.16.238.11
ssh banner@172.16.238.12
sudo -l
```
