## mysql 常用命令


### MYSQL8.0 数据库用户操作命令

#### 1 创建用户并设置密码（“%” 表示可以外网连接，仅本地连接替换 “%” 为 localhost 即可）
```
create user 'userename'@'%' identified by 'password';
```
#### 2 分配权限
```
grant all on *.* to 'username'@'%';
```
#### 3 刷新权限
```
flush privileges;
```
#### 查看权限
```
show grants for 'username'@'%';
```

#### 修改密码
```
ALTER USER 'username'@'%' IDENTIFIED BY 'new password';

```



### 数据库创建以及创建表语句

#### 创建数据库
```
CREATE SCHEMA `databasename` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_bin ;
```
