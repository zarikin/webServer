### MySql
```
sudo apt install mysql-server
sudo systemctl start mysql
- se connecter :
	mysql -u root -p
- créer un utilisateur : 
	CREATE USER 'non-root'@'localhost' IDENTIFIED BY 'password';
- donner privilèges :
	grant all privileges on *.* to bill@localhost identified by 'pass' with grant option;
```
