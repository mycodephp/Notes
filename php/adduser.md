sudo adduser ftp_user_name
sudo chown -R ankesh:ankesh /var/www/dev


Add a New User
 sudo adduser username


Grant Administrative Privileges
 sudo usermod -aG sudo username

 Switch to the New User

su - username
ssh username@your-server-ip  # If accessing remotely

1. Open the sudoers file safely
sudo visudo
2. Grant Full Root Privileges
username ALL=(ALL) ALL
3. Grant Passwordless sudo (Optional)
If you want the user to run sudo commands without entering a password, use:
username ALL=(ALL) NOPASSWD:ALL

4. Restrict User to Specific Commands
username ALL=(ALL) NOPASSWD: /usr/bin/apt, /usr/bin/systemctl restart apache2







