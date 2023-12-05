# Install-LAMP-Linux-Server

# Mengatur Permition Root
```
sudo su
nano /etc/ssh/sshd_config

//kemudian ubahlah PermitRootLogin without-password menjadi   PermitRootLogin yes

nano /etc/ssh/ssh_config

//hilangkan tanda pagar pada PasswordAuthentication yes

passwd root

service ssh reload
```
# install Apache
```
sudo apt install apache2
```
# install mysql
```
sudo apt install mysql-server
```
# Cek Status MySql
```
sudo service mysql status
```
# Mengatur User
```
sudo mysql

alter user 'root'@'localhost' identified with mysql_native_password by 'nanangmrk';

exit

sudo mysql_secure_installation

sudo mysql -u root -p

alter user 'root'@'localhost' identified with auth_socket;
```

# Membuat user baru
```
create user 'nanangmrk'@'localhost' identified by 'nanangmrk';

grant all privileges on *.* to 'nanangmrk'@'localhost';

flush privileges;

exit
```
# install php
```
sudo apt install php libapache2-mod-php php-mysql
```

# untuk melihat php terinstall
```
cd /var/www/html

sudo nano info.php

<?php phpinfo(); ?>
```

# install phpmyadmin
```
sudo apt install phpmyadmin
```
