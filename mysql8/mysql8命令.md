##账户登录
**root账户登录** &nbsp; `mysql --user root -p`
<br>

##数据库操作
**创建** &nbsp; `create database 数据库名`
**选用数据库** &nbsp; `use 数据库名`
**展示现有数据库** &nbsp; `show databases;`
**删除数据库** &nbsp; `drop database 数据库名;`
<br>

##视图操作
**展示全部视图** &nbsp; `show table status where comment='view';`
<br>

##用户
**创建用户** &nbsp; `create user '用户名'@'%' identified by '密码';`
**授予全部权限** &nbsp; `grant all privileges on 数据库名.* to '用户名'@'%';` 
<span style="color:grey">（以上操作需要执行刷新操作：&nbsp; `flush privileges;`）</span>
**查看全部用户** &nbsp; `select * from mysql.user;`
<br>

##密码策略
**查看当前密码策略** &nbsp; `show global variables like '%validate_password%';`
**修改密码策略** &nbsp; `set global validate_password.policy=0;`
<br>

##其他
**执行sql文件** 
* `source 路径/文件名`
* 刷新配置 &nbsp; `flush privileges;`
<br>
