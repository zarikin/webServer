### MySql
```
sudo apt install mysql-server
sudo systemctl start mysql
```
- se connecter :
```
	mysql -u root -p
```
- créer un utilisateur : 
```sql
	CREATE USER 'non-root'@'localhost' IDENTIFIED BY 'password';
```	
- donner privilèges :
```sql
	grant all privileges on *.* to non-root@localhost identified by 'password' with grant option;
```
- retirer le mot de passe root
    - Open & Edit ```/etc/mysql/mysql.conf.d/mysqld.cnf```
    - Add ```skip-grant-tables``` under [mysqld]
    - rédémarrer Mysql
    - se connecter avec ``` mysql -u root -p ```
    - faire les commandes suivantes : 
    ```sql
    use mysql; # use mysql table
    update user set authentication_string=PASSWORD("") where User='root'; # update password to nothing
    update user set plugin="mysql_native_password" where User='root'; # set password resolving to default mechanism for root user
    flush privileges;
    quit;
    ```
    - ```sudo systemctl restart mysql```
    - se connecter avec ```mysql -u root -p```
    

- créer une database :
```sql
CREATE DATABASE databasename;
USE databasename;
```
