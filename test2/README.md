实验一  
姓名：刘成；学号：201610414311  
日期：2018/10/24  
实验目的：学习用户管理 - 掌握管理角色、权根、用户的能力，并在用户之间共享对象。  
创建角色和用户： 
  
    SQL> CREATE ROLE JSS;  
    Role created.  
    SQL> GRANT connect,resource,CREATE VIEW TO JSS;  
    Grant succeeded.  
    SQL> CREATE USER LIUC IDENTIFIED BY 123 DEFAULT TABLESPACE users TEMPORARY TABLESPACE temp;  
    User created.  
    SQL> ALTER USER LIUC QUOTA 50M ON users;授权LIUC用户访问users表空间  
    User altered.  
    SQL> GRANT JSS TO LIUC;  
    Grant succeeded.  
    SQL> exit  
 运行上面代码创建角色为JSS，创建的用户为LIUC，如下图：  
 ![Image text](https://github.com/201610414311/Oracle/blob/master/test2/oracle2.1.png)  
  
    
    创建表mytable和视图myview，插入数据，最后将myview的SELECT对象权限授予hr用户：  
    SQL> show user;  
    USER is "LIUC"  
    SQL> CREATE TABLE mytable (id number,name varchar(50));  
    Table created.  
    SQL> INSERT INTO mytable(id,name)VALUES(1,'zhang'); 
    1 row created.  
    SQL> INSERT INTO mytable(id,name)VALUES (2,'wang'); 
    1 row created.  
    SQL> CREATE VIEW myview AS SELECT name FROM mytable;  
    View created.  
    SQL> SELECT * FROM myview;  
    NAME  
   --------------------------------------------------  
   zhang  
   wang  
   SQL> GRANT SELECT ON myview TO hr;  
   Grant succeeded.  
   SQL>exit  
   运行上面代码如下图：  
   ![Image text]()
