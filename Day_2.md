# Day 2: Temporary User Setup with Expiry Date

As part of the temporary assignment to the Nautilus project, a developer named ammar requires access for a limited duration. To ensure smooth access management, a temporary user account with an expiry date is needed. Here's what you need to do:

> Create a user named `ammar` on `App Server 2` in Stratos Datacenter. Set the expiry date to `2023-12-07`, ensuring the user is created in lowercase as per standard protocol.


## Solution
```sh
ssh tony@173.21.3.20
sudo useradd -e 2023-12-07 ammar
getent passwd anita
sudo chage -l ammar
```
