# Reset_mysql_root_password

Get-service

net stop mysql

get-preocess

stop process -name mysql -force

mysql --skip-grant-tables
or
mysql_safe --skip-grant-tables

mysql

 UPDATE mysql.user SET Password=PASSWORD('password')WHERE User='root'; 
 
 or
 
 UPDATE user SET Password = PASSWORD('password') WHERE User ='root';

CREATE USER 'abx'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON *.* TO 'abx'@'localhost' WITH GRANT OPTION;
flush privileges;

UPDATE user SET Password = PASSWORD('password') WHERE User ='pma';
flush privileges;

open seprate cmd
and try to login



Stop Mysql service by going into Administrative tools > Services


Open Start > Run > cmd (Run as administrator)


Start the server manually using this line:

mysqld -P3306 --skip-grant-tables

In new cmd (Run as administrator) execute :

mysql -P3306 mysql

Execute the following query in mysql client:

update mysql.user set authentication_string=password('new_password') where user='root';
