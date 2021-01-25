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

// .zshrc文件中
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
show dadabase; // 当前数据库的表

use test; // 使用test数据库 

show tables; // 显示当前数据库下的表

show tables from mysql;  // 查表

select database();  查询当前使用的是哪个数据库

// 创建一个只有name id的表
create table stuinfo(
  id int,
  name varchar(20)
);
show tables; // 查看当前数据库下的表

desc stuinfo;  //查看表结构 会显示表的信息

select * from stuinfo; // 检索stuinfo 表中的数据
// 插入id =1 name = 'john'的一条数据
insert into stuinfo (id, name) values (1, 'john');

insert into stuinfo (id, name) values (2,  'rose');

insert into stuinfo (id, name) values (3,  'rose');
// 查询stuinfo下的所有数据
select * from stuinfo;
// 更新id = 1 的那条数据的name为李磊
update stuinfo set name='lilei' where id = 1;
// 从stuinfo中删除 id = 1的那条数据
delete from stuinfo where id =1;


```
