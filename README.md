## Some Useful Command
****************************************************
**setup ubuntu server**
https://www.youtube.com/watch?v=TKLPDbSqOPY

****************************************************
**php server command userfull terminal command**

# useful server command 

 php -v
 sudo a2dismod php7.0.*
 sudo a2dismod php7.*
 sudo a2enmod php7.2
 sudo systemctl restart apache2
Change the command line php version:
sudo update-alternatives --config php

 vs code Update command --->
 sudo apt-get install --only-upgrade code

*********************************************
**Run persistence usb mysql error issue**

sudo service mysql start

Each reboot start: sudo service mysql start

*********************************************
**require rewrite engine on**

In etc/apache2/apache2.conf

<Directory /var/www/>
	Options Indexes FollowSymLinks
	AllowOverride All
	Require all granted
</Directory>

****************************************************
.htaccess
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php/$1 [L]
*********************************************
**fix larave not running without index.php**

in /etc/apache2/sites-enabled/000-default.conf

DocumentRoot /var/www
<Directory />
Options FollowSymLinks
AllowOverride All
</Directory>
<Directory /var/www/>
Options Indexes FollowSymLinks MultiViews
AllowOverride All
Order allow,deny
allow from all
</Directory>

or 

# Below are add by arafat

<Directory /var/www/>
    Options Indexes FollowSymLinks MultiViews
    AllowOverride None
    Order allow,deny
    allow from all
</Directory>



*********************************************
**Reset Mysql Password**

Reset mysql Password

sudo mysql --user=root mysql

flush privileges;


ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';

flush privileges;

https://devanswers.co/how-to-reset-mysql-root-password-ubuntu/

*********************************************
**How to start lampp**
sudo /opt/lampp/lampp start


*********************************************
**Boot loaded grub rescue fix boot**

1. https://askubuntu.com/questions/190763/install-grub-to-ubuntu-partition


*********************************************

# Linux Update Command

**sudo apt-get --only-upgrade install**

for vs code 

sudo apt-get --only-upgrade install code

for Google Chrome

sudo apt-get --only-upgrade install google-chrome-stable

for Sublime Text 

sudo apt-get --only-upgrade install subl

*********************************************
**Usefull terminal Command**

List all recursively::
ls -R > filename1

Take all the database backupusing terminal in the current directory:::
mysqldump -u root -p --all-databases > alldb_backup.sql

Disk Usage: du -hs /path/to/directory

rsync -av

Show Percentages::

rsync -avh --info=progress2 source dest

https://askubuntu.com/questions/802672/how-to-properly-copy-files-from-hard-drive-to-usb-flash-drive-in-tty4-terminal

*********************************************


**Linux-update-without-kernel**

Disable Kernel Updates
sudo apt-mark hold linux-image-generic linux-headers-generic

Updates Apt-Get Local DB
sudo apt-get update

Install Upgrades
sudo apt-get upgrade -y

Enable Kernel Updates
sudo apt-mark unhold linux-image-generic linux-headers-generic

Current version Kernel  is:
4.10.0-041000-generic

*********************************************
**wp smtp issue**
Wp important Plugin :::

https://wordpress.org/plugins/wp-mail-smtp/

**********************************************
**For Simple Use of Git**

For Simple Use of Git

git init
git add .
git commit -am "Taking the project into Git"
git remote add origin https://github.com/arafat-cdr/my-repo-name
git push -f origin master

*****************************************************

