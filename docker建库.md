# docker建库



```
docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=12345678 mysql:5.7

再进去创表创库。

docker exec -it d6ac0290e8772399833123a2594a18f6ead54552feded08d9001dbb7a13a1c52 bash

mysql -u root -p

SQL 语句

create database ctf;

use ctf;

create table user(

 id int(11) primary key auto_increment,

 username varchar(256),

 password varchar(256)

);

然后往里插入数据。

insert into user values(1,'admin',md5('12345678'));
```

