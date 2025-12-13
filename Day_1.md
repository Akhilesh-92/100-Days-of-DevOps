# Day 1: Linux User Setup with Non-Interactive Shell
Create a user with non-interactive shell for your organization on a specific server. This is essential for service accounts and automated processes that don't require interactive login capabilities.

## Solution
```sh
ssh tony@173.21.3.20
sudo useradd -s /sbin/nologin anita
getent passwd anita
```
