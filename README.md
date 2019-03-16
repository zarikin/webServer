# webServer
## How install in linux (with php)
### install
```
sudo apt install -y apache2
sudo apt-get install php libapache2-mod-php
service apache2 start
cd /var/www
sudo chmod 777 -R *
```
After that, we can change the index.html that is in the html folder to index.php and start to code php in the file. Be careful to put the tags:
```
<? Php
echo "here your code";
?>
```
### display errors
go to /etc/php/apache2/php.ini and change :
```
display_errors = Off      by    display_errors = On
display_startup_errors = Off       by      display_startup_errors = On
```
