
add ssl 
https://certbot.eff.org/instructions?ws=apache&os=ubuntufocal (refer)
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
sudo certbot --apache
sudo certbot --apache -d newdomain.com

sudo certbot certonly --apache
sudo certbot renew
certbot certonly --force-renew -d dev.icloudcampus.com
sudo certbot renew --dry-run

/etc/apache2/sites-available/your_domain_ssl.conf
<VirtualHost *:443>
    ServerAdmin webmaster@your_domain.com
    ServerName your_domain.com
    DocumentRoot /var/www/html

    SSLEngine on
    SSLCertificateFile /etc/letsencrypt/live/your_domain.com/fullchain.pem
    SSLCertificateKeyFile /etc/letsencrypt/live/your_domain.com/privkey.pem
    # Additional SSL configurations go here...
</VirtualHost>

multi domin 

sudo nano /etc/apache2/sites-available/school2.example.com.conf
Add this config:
<VirtualHost *:80>
    ServerName school2.example.com
    DocumentRoot /var/www/smart_school_src

    <Directory /var/www/smart_school_src>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/school2_error.log
    CustomLog ${APACHE_LOG_DIR}/school2_access.log combined
</VirtualHost>

Enable site & reload Apache:
sudo a2ensite school2.example.com.conf
sudo systemctl reload apache2

Obtain SSL Certificate:
sudo certbot --apache -d school.hidaya-academy.org


sudo apache2ctl configtest
sudo systemctl restart apache2
sudo certbot --apache --staging -d subdomain.example.com


sudo allow ufw https
sudo a2enmod ssl
