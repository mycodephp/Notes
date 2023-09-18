
add ssl 
https://certbot.eff.org/instructions?ws=apache&os=ubuntufocal (refer)
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
sudo certbot --apache
sudo certbot certonly --apache
sudo certbot renew
certbot certonly --force-renew -d [example.com]
sudo certbot renew --dry-run

sudo allow ufw https
sudo a2enmod ssl
