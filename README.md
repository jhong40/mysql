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
