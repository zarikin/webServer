# webServer
## How install in linux (with php)
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
