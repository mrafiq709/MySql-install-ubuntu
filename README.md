# MySql-install-ubuntu
MySQL Ubuntu

command:
----------
    sudo apt update
    sudo apt install mysql-server
    
For Set Up the password:
------------------------
    sudo mysql_secure_installation utility
    
Advanced(If need):
------------------
    sudo ufw enable
    sudo ufw allow mysql
    
Start MySaql Server:
----------------------
    sudo systemctl start mysql
    sudo systemctl enable mysql
    sudo systemctl restart mysql
    
Log into mysql:
----------------
    /usr/bin/mysql -u root -p

References: https://support.rackspace.com/how-to/installing-mysql-server-on-ubuntu/
