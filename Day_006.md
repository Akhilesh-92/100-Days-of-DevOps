# Day 6: Setup a Cron Job
The `Nautilus` system admins team has prepared scripts to automate several day-to-day tasks. They want them to be deployed on all app servers in Stratos DC on a set schedule. Before that they need to test similar functionality with a sample cron job. Therefore, perform the steps below:

Install cronie package on all `Nautilus` app servers and start crond service.
Add a cron `*/5 * * * * echo hello > /tmp/cron_text` for `root` user.

## Solution
Install the cronie package and start the service
```sh
sudo yum install -y cronie
sudo systemctl start crond
```
Edit the crontab and insert the confguration
```sh
sudo crontab -e
*/5 * * * * echo hello > /tmp/cron_text
```
Verify the configuration wth below command
```sh
sudo crontab -l
```
