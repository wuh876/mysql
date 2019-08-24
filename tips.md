# 常见错误
## 1、mysql8 报错 Unable to load authentication plugin 'caching_sha2_password'
```
 ALTER USER 'root'@'localhost' IDENTIFIED BY 'password' PASSWORD EXPIRE NEVER; #修改加密规则 
 
 ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password'; #更新一下用户的密码 

 FLUSH PRIVILEGES; #刷新权限 

再重置下密码：alter user 'root'@'localhost' identified by 'root';
```
