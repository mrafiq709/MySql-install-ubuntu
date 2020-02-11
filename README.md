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
    or
    sudo mysql // root user
    
Change root password:
-----------------------
    SELECT user,authentication_string,plugin,host FROM mysql.user;
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'new-password';
    FLUSH PRIVILEGES;
    
How to Create a New User:
--------------------------
To create a new MySQL user account, run the following command:

    CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';
    
To grant access from another host, change the hostname part (localhost) with the remote machine IP. For example, to grant access from a machine with IP 10.8.0.5 you would run:

    CREATE USER 'newuser'@'10.8.0.5' IDENTIFIED BY 'user_password';
    
To create a user that can connect from any host, use the '%' wildcard as a host part:
    
    CREATE USER 'newuser'@'%' IDENTIFIED BY 'user_password';

Grand all privileges to a user account on all databases:

    GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';
    FLUSH PRIVILEGES;

References:
-------------
https://support.rackspace.com/how-to/installing-mysql-server-on-ubuntu/

https://linuxize.com/post/how-to-create-mysql-user-accounts-and-grant-privileges/
