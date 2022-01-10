sudo apt install certbot python3-certbot-apache

change ServerName in 000-default.conf

xxx.com

> using apache

sudo certbot --apache


> or (using DNS and HTML file)

sudo certbot certonly --manual -d videoo.org -d *.videoo.org

