实验一  
姓名：刘成；学号：201610414311  
日期：2018/10/24  
实验目的：学习用户管理 - 掌握管理角色、权根、用户的能力，并在用户之间共享对象。  
如下图，我创建的角色为JSS，创建的用户为LIUC  
SQL> CREATE ROLE JSS;  
Role created.  
SQL> GRANT connect,resource,CREATE VIEW TO JSS;  
Grant succeeded.  
SQL> CREATE USER LIUC IDENTIFIED BY 123 DEFAULT TABLESPACE users TEMPORARY TABLESPACE temp;  
User created.  
SQL> ALTER USER LIUC QUOTA 50M ON users;  
User altered.  
SQL> GRANT JSS TO LIUC;  
Grant succeeded.  
SQL> exit  
 运行上面代码创建角色为JSS，创建的用户为LIUC，如下图：  
 ![Image text](https://github.com/201610414311/Oracle/edit/master/test2/oracle2.1)  
