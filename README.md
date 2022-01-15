# Reset_mysql_root_password

Stop Mysql service by going into Administrative tools > Services


Open Start > Run > cmd (Run as administrator)


Start the server manually using this line:

mysqld -P3306 --skip-grant-tables

In new cmd (Run as administrator) execute :

mysql -P3306 mysql

Execute the following query in mysql client:

update mysql.user set authentication_string=password('new_password') where user='root';
