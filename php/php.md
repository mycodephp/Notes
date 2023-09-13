
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

 php comuntiction
 sudo apt install php-mysql
