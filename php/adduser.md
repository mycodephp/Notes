sudo adduser ftp_user_name
sudo chown -R ankesh:ankesh /var/www/dev


Add a New User
 sudo adduser username


Grant Administrative Privileges
 sudo usermod -aG sudo username

 Switch to the New User

su - username
ssh username@your-server-ip  # If accessing remotely


