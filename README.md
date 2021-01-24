# mysql-study  mysql-study
### mysql安装

### 数据库启动 停止
```
启动MySQL服务
sudo /usr/local/MySQL/support-files/mysql.server start

停止MySQL服务
sudo /usr/local/mysql/support-files/mysql.server stop

重启MySQL服务
sudo /usr/local/mysql/support-files/mysql.server restart

alias mysql=/usr/local/mysql/bin/mysql
alias mysqladmin=/usr/local/mysql/bin/mysqladmin
```

### mysql 服务的登录和退出
```
mysql [-h 127.0.0.1 -P 3306] -u root -p  // 直接回车 敲密码 或者直接在 -p后加密码
exit // 退出
```
### mysql的常用命令
```
show dadabase; 

use test; // 使用test 

show tables; 

show tables from mysql;  // 查表

select database();  查询当前使用的数据库

create table stuinfo(
  id int,
  name varchar(20)
);
show tables; // 查看当前数据库下的表

desc stuinfo;  //查看表结构

select * from stuinfo; // 查数据

insert into stuinfo (id, name) values (1, 'john');

insert into stuinfo (id, name) values (2,  'rose');

insert into stuinfo (id, name) values (3,  'rose');

select * from stuinfo;

update stuinfo set name='lilei' where id = 1;

delete from stuinfo where id =1;
```
