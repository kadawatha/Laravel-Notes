# Laravel-Notes

<h5> Laravel Old Version Download </h5>

# composer create-project laravel/laravel your-project-name 5.0

<hr>
    return view('profile',array('user'=>Auth::user()))->with('years',Group::all())->with('occupations',Occupation::all());



laravel foreach loop in controller



```
foreach ($product as $p) {
echo $p->sku;
}
```
<p>Laravel Auth in Controller </p>

``` 
public function allOrders(){

        $user = Auth::user();
        
        $id = Auth::id();
        
        $Orders=DB::select("SELECT * FROM orders WHERE users_id = '$id'");
        return view('checkout.review_order_2',compact('Orders','user'));
        
    }
    
```

How do we set a custom port for test server? (microservice)

 php artisan serve --port=8080

<hr>

php artisan serve --port=8001


<h3>ErrorException file_put_contents failed to open stream: No such file or directory</h3>


```

The best way to solve this problem is, go to directory laravel/bootstrap/cache and delete config.php file. or you can rename it as well like config.php.old And your problem will be fix. Happy coding :-


```





<hr>


    php artisan make:model Sample -mcr


<hr>


    php artisan make:model Category -m



<hr>

### laravel auth


```

composer require laravel/ui
php artisan ui bootstrap --auth

```

```

server {
    listen 80;
    listen [::]:80;

    root /var/www/crazzyartist.com/html;
    index index.php index.html index.htm index.nginx-debian.html;

    server_name gssce.com www.gssce.com;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
    }

    location ~ /\.ht {
            deny all;
    }
}


```


## full permision to folder

```

sudo mkdir /var/szDirectoryName
sudo chmod a+rwx /var/szDirectoryName


```

`show databases;`
`CREATE DATABASE soap_store;`

``
### Fix Brightness Using a Software


```

sudo add-apt-repository ppa:apandada1/brightness-controller
sudo apt update
sudo apt install brightness-controller


```

### mac icon for ubuntu

```

http://ubuntuhandbook.org/index.php/2020/01/install-mac-os-mojave-theme-ubuntu-19-10/

```



### nodejs install



```

node install

sudo apt update

sudo apt install nodejs

sudo apt install npm

nodejs -v

npm -v

sudo npm install -g npm 

npm -v

hash -d npm



```

### remove nodejs 


```


sudo apt-get purge nodejs

sudo apt-get purge --auto-remove nodejs


```

### install nodejs latest version

```


curl -sL https://deb.nodesource.com/setup_10.x -o nodesource_setup.sh


sudo bash nodesource_setup.sh


sudo apt install nodejs


```



### ssl install

```


sudo certbot --nginx


Select the appropriate numbers separated by commas and/or spaces, or leave input
blank to select all options shown (Enter 'c' to cancel): 2

Select the appropriate number [1-2] then [enter] (press 'c' to cancel): 1


```


<p> authentication genarate Laravel 6 </p>



```

composer require laravel/ui "^1.0" --dev

php artisan ui react --auth


```

<h3> Laravel Active Manu  </h3>

```

     <div class="menu">
                <div id="cssmenu">
                    <ul>
                        <li class="{{(request()->segment(1) == '') ? 'active' : '' }}"><a href="{{url('/')}}"><span>Home</span></a></li>
                        <li class="{{(request()->segment(1) == 'about') ? 'active' : '' }}"><a href="{{url('about')}}"><span>About</span></a></li>
                        <li class="{{(request()->segment(1) == 'gallery') ? 'active' : '' }}"><a href="{{url('gallery')}}"><span>Gallery</span></a></li>
                        <li class="{{(request()->segment(1) == 'contact-page') ? 'active' : '' }}"><a href="{{url('contact-page')}}"><span>Contact</span></a></li>
                    </ul>
                </div>
    </div>
            

```

<p> variable inside asset </p>

```
{{ asset('img/backgrounds/' . $background . '.jpg') }}

```

<hr>

### PasswordAuthentication with a value of Yes. 

```
$ sudo vim /etc/ssh/sshd_config

```

```

PasswordAuthentication no
press i for insert mode


```

```

[escape] :wq

```

```

$ sudo systemctl restart ssh
Some systems make require
$ sudo systemctl restart sshd

```
<hr>

### for wordpress routing


```


location / {
        # First attempt to serve request as file, then
        # as directory, then fall back to displaying a 404.
        try_files $uri $uri/ /index.php?q=$uri&$args; 
        #try_files $uri $uri/ =404;
        # Uncomment to enable naxsi on this location
        # include /etc/nginx/naxsi.rules
    }



```

### for wordpress plugin

```

chown -Rf www-data.www-data /var/www/html/


```

<hr>

### uninstall apche


```

sudo apt-get --purge remove apache2
sudo apt-get remove apache2-common

```

### install apche


```
sudo apt-get install apache2

sudo apt install php libapache2-mod-php

sudo apt install php7.0-mbstring


```



### apche notes


```
sudo systemctl stop apache2.service

sudo systemctl start apache2.service

sudo systemctl restart apache2.service

sudo systemctl reload apache2.service

```



<hr>

### uninstall nginx


```

sudo apt-get remove nginx nginx-common

```

```

sudo apt-get purge nginx nginx-common

```

```

sudo apt-get autoremove

```

## get permistion

```

sudo chmod -R 777 storage

sudo chmod  -R 777 bootstrap

```


## deploy to digital ocean

---
title: Setting Up Laravel in Ubuntu / DigitalOcean
keywords: servers, laravel, coderstape, coder's tape
description: Let's take a look at settting up a server from scratch for Laravel.
date: April 1, 2019
tags: servers, laravel
permalink: setting-up-laravel-in-ubuntu-digitalocean
img: https://coderstape.com/storage/uploads/GZTXUbyGum2xeUZM9qBD5aPv8EKLwG3C8RGcRon4.jpeg
author: Victor Gonzalez
authorlink: https://github.com/vicgonvt

---

In this post, we are looking at the steps necessary to create an Ubuntu droplet in DigitalOcean from scratch. This is the companion guide to the video series in Laravel 5.8 from scrath. Follow along with those to get the video guide.

Part 1
[https://coderstape.com/lesson/112-deployment-basic-server-setup-part-1](https://coderstape.com/lesson/112-deployment-basic-server-setup-part-1)

Part 2
[https://coderstape.com/lesson/113-deployment-basic-server-setup-part-2](https://coderstape.com/lesson/113-deployment-basic-server-setup-part-2)

Part 3
[https://coderstape.com/lesson/114-deployment-basic-server-setup-part-3](https://coderstape.com/lesson/114-deployment-basic-server-setup-part-3)

## Getting Started

+ Create droplet with Ubuntu 18.10
+ `ssh root@[DROPLET IP ADDRESS]`
+ Get password from your email
+ Change password on first login
+ `adduser laravel`
+ Enter password and other information
+ `usermod -aG sudo laravel`

## Locking Down to SSH Key only (Extremely Important)

+ In your local machine, `ssh-keygen`
+ Generate a key, if you leave passphrase blank, no need for password
+ `ls ~/.ssh` to show files in local machine
+ Get the public key, `cat ~/.ssh/id_rsa.pub`
+ Copy it 
+ `cd ~/.ssh` and `vim authorized_keys`
+ Paste key
+ Repeat steps for laravel user
+ `su laravel` then `mkdir ~/.ssh` fix permissions `chmod 700 ~/.ssh`
+ `vim ~/.ssh/authorized_keys` and paste key
+ `chmod 600 ~/.ssh/authorized_keys` to restrict this from being modified
+ `exit` to return to root user

## Disable Password from Server

+ `sudo vim /etc/ssh/sshd_config`
+ Find PasswordAuthentication and set that to `no`
+ Turn on `PubkeyAuthentication yes`
+ Turn off `ChallengeResponseAuthentication no`
+ Reload the SSH service `sudo systemctl reload sshd`
+ Test new user in a new tab to prevent getting locked out

## Setting Up Firewall

+ View all available firewall settings
+ `sudo ufw app list`
+ Allow on OpenSSH so we don't get locked out
+ `sudo ufw allow OpenSSH`
+ Enable Firewall
+ `sudo ufw enable`
+ Check the status
+ `sudo ufw status`

## Install Linux, Nginx, MySQL, PHP

### Nginx

+ `sudo apt update` enter root password
+ `sudo apt install nginx` enter Y to install
+ `sudo ufw app list` For firewall
+ `sudo ufw allow 'Nginx HTTP'` to add NGINX
+ `sudo ufw status` to verify change
+ Visit server in browser

### MySQL

+ `sudo apt install mysql-server` enter Y to install
+ `sudo mysql_secure_installation` to run automated securing script
+ Press N for VALIDATE PASSWORD plugin
+ Set root password
+ Remove anonymous users? `Y`
+ Disallow root login remotely? `N`
+ Remove test database and access to it? `Y`
+ Reload privilege tables now? `Y`
+ `sudo mysql` to enter MySQL CLI
+ `SELECT user,authentication_string,plugin,host FROM mysql.user;` to verify root user's auth method
+ `ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'STRONG_PASSWORD_HERE';` to set a root password
+ `SELECT user,authentication_string,plugin,host FROM mysql.user;` to verify root user's auth method
+ `FLUSH PRIVILEGES;` to apply all changes
+ `mysql -u root -p` to access db from now on, enter password `STRONG_PASSWORD_HERE`

### PHP & Basic Nginx

+ `sudo add-apt-repository universe` to add software repo
+ `sudo apt install php-fpm php-mysql` to install the basic PHP software
+ `sudo vim /etc/nginx/sites-available/YOUR.DOMAIN.COM`
```
server {
        listen 80;
        root /var/www/html;
        index index.php index.html index.htm index.nginx-debian.html;
        server_name YOUR.DOMAIN.COM;

        location / {
                try_files $uri $uri/ =404;
        }

        location ~ \.php$ {
                include snippets/fastcgi-php.conf;
                fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
        }

        location ~ /\.ht {
                deny all;
        }
}
```
+ `sudo ln -s /etc/nginx/sites-available/YOUR.DOMAIN.COM /etc/nginx/sites-enabled/` to create symlink to enabled sites
+ `sudo unlink /etc/nginx/sites-enabled/default` to remove default link
+ `sudo nginx -t` test the whole config
+ `sudo systemctl reload nginx` to apply all changes
+ `sudo vim /var/www/html/info.php` to start a new PHP file, fill it with <?php phpinfo();
+ `sudo rm /var/www/html/info.php` optional command to get rid of test file

## Let's Dial in The Laravel Ecosystem

+ `sudo apt-get install php7.2-mbstring php7.2-xml composer unzip`
+ `mysql -u root -p` Login to create the Laravel DB
+ `CREATE DATABASE laravel DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;`
+ `GRANT ALL ON laravel.* TO 'laraveluser'@'localhost' IDENTIFIED BY 'password';`
+ `FLUSH PRIVILEGES;`
+ `exit`
+ `cd /var/www/html`, `sudo mkdir -p first-project`
+ `sudo chown laravel:laravel first-project`
+ `git clone https://github.com/coderstape/laravel-58-from-scratch.git .`
+ `composer install`
+ `cp .env.example .env`, and then `vim .env`

```
APP_NAME=Laravel
APP_ENV=production
APP_KEY=
APP_DEBUG=false
APP_URL=http://YOUR.DOMAIN.COM

LOG_CHANNEL=stack

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=root
DB_USERNAME=laravel
DB_PASSWORD=STRONG_PASSWORD_HERE
```

+ `php artisan migrate`
+ `php artisan key:generate` to generate the key
+ `sudo chgrp -R www-data storage bootstrap/cache` fix permissions
+ `sudo chmod -R ug+rwx storage bootstrap/cache` fix permissions
+ `sudo chmod -R 755 /var/www/html/first-project` fix permissions
+ `chmod -R o+w /var/www/html/first-project/storage/` fix permission


### sudo chmod -R 777 storage


## Modify Nginx

+ `sudo vim /etc/nginx/sites-available/YOUR.DOMAIN.COM`
~~~
server {
    listen 80;
    listen [::]:80;

    root /var/www/html/first-project/public;
    index index.php index.html index.htm index.nginx-debian.html;

    server_name YOUR.DOMAIN.COM;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
    }

    location ~ /\.ht {
            deny all;
    }
}
~~~

+ `sudo nginx -t`
+ `sudo systemctl reload nginx` reload Nginx

## Let's Encrypt

+ `sudo add-apt-repository ppa:certbot/certbot` to get repo
+ `sudo apt install python-certbot-nginx` to install
+ `sudo certbot certonly --webroot --webroot-path=/var/www/html/quickstart/public -d example.com -d www.example.com`
+ `sudo certbot certonly --webroot --webroot-path=/var/www/html/first-project/public -d YOUR.DOMAIN.COM`

### Final mod for Nginx

+ `sudo vim /etc/nginx/sites-available/YOUR.DOMAIN.COM`

~~~
server {
    listen 80;
    listen [::]:80;

    server_name YOUR.DOMAIN.COM;
    return 301 https://$server_name$request_uri;
}

server {
    listen 443 ssl http2;
    listen [::]:443 ssl http2;
    server_name YOUR.DOMAIN.COM;
    root /var/www/html/first-project/public;

    ssl_certificate /etc/letsencrypt/live/YOUR.DOMAIN.COM/fullchain.pem;
	ssl_certificate_key /etc/letsencrypt/live/YOUR.DOMAIN.COM/privkey.pem;
    
    ssl_protocols TLSv1.2;
	ssl_ciphers ECDHE-RSA-AES256-GCM-SHA512:DHE-RSA-AES256-GCM-SHA512:ECDHE-RSA-AES256-GCM-SHA384:DHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-SHA384;
	ssl_prefer_server_ciphers on;

	add_header X-Frame-Options "SAMEORIGIN";
	add_header X-XSS-Protection "1; mode=block";
	add_header X-Content-Type-Options "nosniff";

	index index.php index.html index.htm index.nginx-debian.html;

    charset utf-8;

    location / {
            try_files $uri $uri/ /index.php?$query_string;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.2-fpm.sock;
    }

    location ~ /\.ht {
            deny all;
    }

    location ~ /.well-known {
            allow all;
    }
}
~~~

+ `sudo nginx -t`
+ `sudo ufw app list` For firewall
+ `sudo ufw allow 'Nginx HTTPS'` to add NGINX
+ `sudo ufw status` to verify change
+ `sudo systemctl reload nginx` reload Nginx

## Extra Credit

Let's make the prompt pretty

+ `sudo apt-get install zsh` to install ZSH
+ `zsh --version` to confirm install
+ `whereis zsh` to find out where it is
+ `sudo usermod -s /usr/bin/zsh $(whoami)` to make Zsh default
+ `sudo reboot` to reapply all changes
+ `2` to populate a default file
+ `sudo apt-get install powerline fonts-powerline` to install powerline
+ `sudo apt-get install zsh-theme-powerlevel9k` to install Theme
+ `echo "source /usr/share/powerlevel9k/powerlevel9k.zsh-theme" >> ~/.zshrc` to enable the theme in your Zshrc
+ `exit` and login again to see the new theme
+ `sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"` for Oh My Zsh
+ `echo "source /usr/share/powerlevel9k/powerlevel9k.zsh-theme" >> ~/.zshrc` to re-enable 9K
