# Day 9: Debugging MariaDB Issues
There is a critical issue going on with the Nautilus application in Stratos DC. The production support team identified that the application is unable to connect to the database. After digging into the issue, the team found that mariadb service is down on the database server.

## Solution
First, stop the mariadb service and remove the contents of mysql folder
```sh
sudo systemctl stop mariadb
sudo rm -rf /var/lib/mysqld/mysql/*
```
Install MariaDB and start the service
```sh
sudo mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
sudo systemctl start MariaDB
```
