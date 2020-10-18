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
```
	CREATE USER 'non-root'@'localhost' IDENTIFIED BY 'password';
```	
- donner privilèges :
```
	grant all privileges on *.* to bill@localhost identified by 'pass' with grant option;
```
- retirer le mot de passe root
    - Open & Edit ```/etc/mysql/mysql.conf.d/mysqld.cnf```
    - Add skip-grant-tables under [mysqld]
    - rédémarrer Mysql
    - se connecter avec ``` mysql -u root -p ```
