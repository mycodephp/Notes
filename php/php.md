
notes
sudo apt install php

sudo apt install php-xml -y
sudo apt install php-mbstring -y
sudo apt install php-curl -y
sudo apt install php-intl -y
sudo apt-get install php-soap -y
sudo apt-get install php-zip -y
apt-get install php-gd -y
apt-get install zip -y

sudo apt install graphviz aspell ghostscript clamav php-pspell php-curl php-gd php-intl php-mysql php-xml php-xmlrpc php-ldap php-zip php-soap php-mbstring
sudo apt install -y php8.1 php8.1-gd php8.1-sqlite3 php8.1-curl php8.1-zip php8.1-xml php8.1-mbstring php8.1-mysql php8.1-bz2 php8.1-intl php-smbclient php8.1-imap php8.1-gmp php8.1-bcmath libapache2-mod-php8.1 php-gd php-soap
 nano /var/www/public_html/php.php
<?php

// Show all information, defaults to INFO_ALL
phpinfo();

// Show just the module information.
// phpinfo(8) yields identical results.
phpinfo(INFO_MODULES);
?>

nano /etc/php/8.1/apache2/php.ini
max_input_vars = 5000


mysql
mysql install 
sudo apt update
sudo apt install mysql-server
sudo systemctl start mysql.service
sudo mysql
CREATE USER 'moodle-user'@'localhost' IDENTIFIED BY 'moodle-user@123';
 GRANT ALL PRIVILEGES ON *.* TO 'moodle-user'@'localhost';
 FLUSH PRIVILEGES;

//////////

php8.2
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php8.2 -y
sudo apt-get install -y php8.2-cli php8.2-common php8.2-fpm php8.2-mysql php8.2-zip php8.2-gd php8.2-mbstring php8.2-curl php8.2-xml php8.2-bcmath php8.2-intl  php8.2-soap

Alter root pwd
sudo mysql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root';
exit
mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED WITH auth_socket;
//////////

sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
port           = 3306
bind-address            = 0.0.0.0
sudo service mysql restart
sudo ufw allow 3306
sudo ufw allow from  localip to any port 3306

 php comuntiction
 sudo apt install php-mysql

allow
 CREATE USER 'admin'@'%' IDENTIFIED BY 'root@root123';
 ALTER USER 'admin'@'%' IDENTIFIED WITH mysql_native_password BY 'mysqlUsernamePassword';
GRANT ALL PRIVILEGES ON *.* TO 'admin'@'%';
FLUSH PRIVILEGES;

select user,host from mysql.user;
version change
sudo a2dismod php7.4
sudo a2enmod php8.1
sudo apt install php7.4-mysql
custam version install
sudo apt-get update
sudo apt -y install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
sudo apt -y install php7.4
php -v
sudo apt-get install -y php7.4-cli php7.4-json php7.4-common php7.4-mysql php7.4-zip php7.4-gd php7.4-mbstring php7.4-curl php7.4-xml php7.4-bcmath  php7.4-soap php7.4-intl php7.4-xmlrpc
SELECT user, plugin FROM mysql.user;
ALTER USER 'username'@'localhost' IDENTIFIED WITH 'mysql_native_password' BY 'password';


