# script-frankenphp
```bash
sudo apt-get update && sudo apt-get upgrade -y
sudo apt install zip unzip curl -y
sudo apt-get update
sudo apt-get -y install lsb-release ca-certificates curl apt-transport-https
sudo curl -sSLo /tmp/debsuryorg-archive-keyring.deb https://packages.sury.org/debsuryorg-archive-keyring.deb
sudo dpkg -i /tmp/debsuryorg-archive-keyring.deb
sudo sh -c 'echo "deb [signed-by=/usr/share/keyrings/deb.sury.org-php.gpg] https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list'
sudo apt-get update
sudo apt install php8.4 php8.4-cli php8.4-fpm php8.4-{bz2,curl,mbstring,intl,xml} -y
php -v
curl https://frankenphp.dev/install.sh | sh
sudo mv frankenphp /usr/local/bin/
mkdir -p ~/my-app && cd ~/my-app
echo '<?php echo "Hello, FrankenPHP!"; ?>' > index.php
sudo frankenphp php-server
```
Sumber : <br>
https://www.tecmint.com/install-frankenphp-on-ubuntu/ <br>
https://php.watch/articles/php-84-install-upgrade-guide-debian-ubuntu
