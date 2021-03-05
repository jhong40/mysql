# mysql
### Install
```
apt update
apt install mysql-server -y
mysql --version
systemctl status mysql
mysql -u root -p
```
### Create DB, Table - CRUD operation
```
show databases;
create database student;
use student;
create table class (id int, name varchar(50), gpa float);
describe class;
insert into class values (11, 'bilogy',4.8);
select * from class;

source ~/tdata.sql
exit 
quit
```
### Remote access
/etc/mysql/mysql.conf.d
bind-address        = 192.168.1.209
netstat -tulpn

```
mysql> CREATE USER 'user'@'%' IDENTIFIED BY 'xxxx';
Query OK, 0 rows affected (0.00 sec)

mysql> GRANT ALL PRIVILEGES ON *.* TO 'user'@'%' WITH GRANT OPTION;
Query OK, 0 rows affected (0.00 sec)

mysql> FLUSH PRIVILEGES;
```

remote server:
```
mysql -u user  -h 192.168.1.209 -p
```
