
notes
sudo apt install php

sudo apt install php-xml
sudo apt install php-mbstring
sudo apt install php-curl
sudo apt install php-intl
apt-get install php-soap

nano /etc/php/8.1/apache2
max_input_vars = 5000


mysql
mysql install 
sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql.service
sudo mysql
CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'root';
 GRANT ALL PRIVILEGES ON *.* TO 'newuser'@'localhost';
 FLUSH PRIVILEGES;

sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
port           = 3306
bind-address            = 0.0.0.0
sudo service mysql restart
sudo ufw allow 3306
sudo ufw allow from  localip to any port 3306

 php comuntiction
 sudo apt install php-mysql

allow
 CREATE USER 'admin'@'%' IDENTIFIED BY 'root@123';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'%';
FLUSH PRIVILEGES;

select user,host from mysql.user;
version change
sudo a2dismod php5.6
sudo a2enmod php7.2
sudo apt install php7.4-mysql

