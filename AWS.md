# AWS

> in security group, add inbound tcp protocol

```bash
chmod 400 key.pem
ssh -i "key.pem" ubuntu@ec2-52-24-254-18.us-west-2.compute.amazonaws.com
```

```bash
sudo apt-get update
sudo apt-get install lamp-server^

cd /var/www
sudo chown ubuntu:ubuntu -R html
chmod 755 -R html
```

> chnage instance security groups (allow all http traffic)

> configure mysql and phpmyadmin

```bash
sudo mysql_secure_installation
sudo apt-get install phpmyadmin
sudo nano /etc/apache2/apache2.conf
```

> add below line in the end.

```
Include /etc/phpmyadmin/apache.conf
```

```bash
sudo service apache2 restart
```

>  create user and set privileges

```bash
CREATE USER 'webuser'@'localhost' IDENTIFIED BY 'o&9neg@J5X3uW2tM';

GRANT ALL PRIVILEGES ON * . * TO 'webuser'@'localhost';

FLUSH PRIVILEGES;

..

note:

login with default (no password)
sudo mysql -u root (-p)

then create users with native password option
e.g. 
ALTER USER 'webuser'@'localhost' IDENTIFIED WITH mysql_native_password BY 'o&9neg@J5X3uW2tM';
```

> configure buddy and use SFTP for deploy
>
> user: ubuntu
>
> password: ssh key
>
> directory: /var/www/html

> install composer

```bash
cd /var/www/html
sudo apt-get install php-mbstring php-dom
sudo apt install wget php-zip unzip
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
HASH="$(wget -q -O - https://composer.github.io/installer.sig)"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer
```

> install laravel dependencies

```bas
composer install
```

> create .env file
>
> change storage folder permission

```bash
sudo chmod 777 -R storage/
```


> edit apache

sudo nano /etc/apache2/sites-available/nano 000-default.conf

```bash
 <Directory /var/www/html>
    Options Indexes FollowSymLinks MultiViews
    AllowOverride All
    Require all granted
</Directory>

```

> enable redwrite mod
```bash
sudo a2enmod rewrite
```

> restart apache2

```bash
sudo service apache2 restart
```




