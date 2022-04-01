# Install PowerDNS and Mysql on Freebsd12


# Install PowerDNS and Mysql on FreeBSD 12

## Database Installation

```bash
pkg install mysql56-server

sysrc mysql_server="YES"

service mysql-server restart
```

## Database and User Configuration

``` bash
$ mysql

mysql> create database powerdns charset = utf8;

mysql> CREATE USER 'powerdns'@'localhost' IDENTIFIED BY 'XianAdmin';

###mysql> GRANT ALL PRIVILEGES ON powerdns.* TO '%' WITH GRANT OPTION;###
mysql> grant all privileges on powerdns.* to 'powerdns'@'localhost' IDENTIFIED BY 'XianAdmin';


mysql> FLUSH PRIVILEGES;


#For security, we also give the main admin password

$ mysqladmin -u root password "PASSWORD_OF_ROOT"
```

## Install powerdns

``` bash
pkg install powerdns
```

## Reference
* [How to manage MySQL databases and users from the command line](https://www.a2hosting.com/kb/developer-corner/mysql/managing-mysql-databases-and-users-from-the-command-line)
* [PowerDNS, PowerAdmin with Mysql in Freebsd 10.1](http://blog.v-live.pl/category/sieci/dns/)
