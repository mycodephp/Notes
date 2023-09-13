#Let’s begin by updating the local package index to reflect the latest upstream changes:
   sudo apt update
#Then, install the apache2 package:
   sudo apt install apache2
#Adjusting the Firewall
  sudo ufw app list
  #Output
Available applications:
  Apache
  Apache Full
  Apache Secure
  OpenSSH
$ Apache: This profile opens only port 80 (normal, unencrypted web traffic)
$ Apache Full: This profile opens both port 80 (normal, unencrypted web traffic) and port 443 (TLS/SSL encrypted traffic)
$ Apache Secure: This profile opens only port 443 (TLS/SSL encrypted traffic)
$ It is recommended that you enable the most restrictive profile that will still allow the traffic you’ve configured. Since we haven’t configured SSL for our server yet in this guide, we will only need to allow traffic on port 80:
  
  sudo ufw allow 'Apache'
 
  sudo ufw status
  
  Output
Status: active

To                         Action      From
--                         ------      ----
OpenSSH                    ALLOW       Anywhere                  
Apache                     ALLOW       Anywhere                
OpenSSH (v6)               ALLOW       Anywhere (v6)             
Apache (v6)                ALLOW       Anywhere (v6)

#cheack  status
sudo systemctl status apache2

hostname -I
When you have your server’s IP address, enter it into your browser’s address bar:

http://your_server_ip

# Managing the Apache Process
sudo systemctl stop apache2
sudo systemctl start apache2
sudo systemctl reload apache2
sudo systemctl disable apache2
sudo systemctl enable apache2
# Virtual Hosts (Recommended)





