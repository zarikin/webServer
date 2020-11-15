# webServer
## How install in linux (with php)
### install
```
sudo apt install -y apache2
sudo apt-get install -y php libapache2-mod-php
sudo apt install -y php-mysql
sudo apt install php-common php-cli php-bz2 php-curl php-gd php-intl php-json php-readline php-xml php-zip php-fpm php-bcmath php-mbstring
service apache2 start
cd /var/www
sudo chmod 777 -R *
```
After that, we can change the index.html that is in the html folder to index.php and start to code php in the file. Be careful to put the tags:
```
<?php
echo "here your code";
?>
```
### display errors
go to /etc/php/apache2/php.ini and change :
```
display_errors = Off      by    display_errors = On
display_startup_errors = Off       by      display_startup_errors = On
```

## To generate QR code
```
sudo apt-get install php-gd
service apache2 restart
```
Download : [PHP QR code](https://sourceforge.net/projects/phpqrcode/files/)

Unzip and place the folder in the same directory than the .php files.
Then to generate, in the php file :
```
include "phpqrcode/qrlib.php";
QRcode::png('Bonsoir', 'test.png'); //generate qr code
echo "<img src='test.png'/>"; //to display image
```

### changer de version php
```
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php7.3
sudo a2dismod php7.2
sudo a2enmod php7.3
sudo apt-get install -y php libapache2-mod-php
sudo apt install -y php-mysql
sudo apt install php7.3-common php7.3-cli php7.3-bz2 php7.3-curl php7.3-gd php7.3-intl php7.3-json php7.3-readline php7.3-xml php7.3-zip php7.3-fpm php7.3-bcmath php7.3-mbstring
sudo service apache2 restart
```
