
add ssl 
https://certbot.eff.org/instructions?ws=apache&os=ubuntufocal (refer)
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
sudo certbot --apache
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

sudo apache2ctl configtest
sudo systemctl restart apache2
sudo certbot --apache --staging -d subdomain.example.com


sudo allow ufw https
sudo a2enmod ssl
