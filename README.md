# tutorial-list
Merupakan tutorial-tutorial yang pernah saya gunakan

```
Cara Menulis di GitHub :
 - https://help.github.com/articles/markdown-basics/
 - https://github.com/jadejs/jade/blob/gh-pages/src/pages/tutorial.jade
Cara Remote Github dengan Command Line :
 - git init
 - git add answer atau git add * //disini answer merupakan folder yg ingin di upload atau untuk add semuanya
 - git commit -m "First Commit" //Ini untuk commit file ke repo lokal
 - git remote add origin https://github.com/nmfzone/yourproject.git //project yg akan di remote
 - git push -u origin master //ini untuk submit repo lokal ke repo online github

Apabila ada file di repo github yg tidak ada di repo lokal :
 - git pull https://github.com/nmfzone/yourproject.git
 - atau git pull origin master

Merubah/Menambah repo github :
 - git remote set-url origin git@github.com:username/projectname.git
 
Menghapus remote repo github :
 - git remote rm origin
```

# Website Penting
```
##### VPS
https://koding.com/IDE/koding-vm-0/my-workspace
##### HerokuApp
https://dashboard.heroku.com/apps
```

# Tutorial UBUNTU
```
http://www.unixmen.com/install-lemp-server-nginx-mysql-mariadb-php-phpmyadmin-ubuntu-14-1014-0413-10/

http://blog.andzhar.com/2014/11/12/125234/hhvm-nginx-di-ubuntu-server-14-04/

http://blog.andzhar.com/2014/12/11/152615/instalasi-composer-di-hhvm/

http://culttt.com/2013/06/17/setting-up-vagrant-with-laravel-4/

https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-virtual-hosts-server-blocks-on-ubuntu-12-04-lts--3

#### Install Vagrant di Ubuntu :
	>>>>> https://scotch.io/tutorials/getting-started-with-laravel-homestead
	- Buat sebuah folder terserah, misalnya dengan nama Project (mkdir Project)
	di directory /var/www/html
	- Kemudian berpindah ke direktory tersebut (cd Project)
	- Kemudian download vagrant dengan menggunakan perintah :
		vagrant box add laravel/homestead
	- Selagi menunggu download selesai, kita beralih misal ke terminal yang lain. Masih di directory
	yang sama seperti tadi. Ketikkan perintah :
		git clone git@github.com:laravel/homestead.git Homestead
	- Kemudian, setelah selesai mendownload, ketikkan perintah :
		homestead init
		ssh-keygen -t rsa -C "youremail@email.com"
	- Setelah itu beralihlah (defaultnya) ke ~/.homestead kemudian buka Homestead.yaml. Kemudian
	atur authorize, keys, folders dan sites.
	- Kemudian beralih ke direktori awal yaitu direktori project anda tadi
	(cd /var/www/html/Project) kemudian ketikkan perintah :
		vagrant init
	- Setelah itu buka Vagrantfile (vim Vagrantfile), setelah itu rubah :
		dari >> config.vm.box = "base";
		menjadi >> config.vm.box = "laravel/homestead";
	- Done, terakhir tinggal menghidupkan vagrant yaitu dengan perintah :
		vagrant up

#### Setting Environment di Ubuntu :
	- Jika dalam keadaan biasa (belum login), maka lokasi environment berada di /home/NAMA_USER/ , maka
	untuk menambahkan environment yaitu dengan menambahkan perintah export
	di .profile (/home/NAMA_USER/.profile) :
	
			export PATH=$HOME/.composer/vendor/bin:$PATH
	
		kemudian jalankan perintah ". ~/.profile" (tanpa tanda petik)
		kemudian cek dengan perintah "echo $PATH", kalau sudah muncul berarti berhasil :)
	
	- Namun jika dalam keadaan sudah login (sudo su), maka lokasi environment yaitu berada di
	/etc/environment , maka untuk menambahkan environment tinggal tambahkan saja di dalam PATH
	yang ada disitu. Khusus untuk JAVA (maybe), berikan tambahkan line khusus dibawah PATH yaitu
	JAVA_HOME..kemudian berikan value di belakangnya :
	
			PATH="bla bla bla"
			JAVA_HOME="JAVA_PATH" (ganti JAVA path dengan lokasi JAVA misalnya /usr/lib/jvm/java-8-openjdk-amd64
			
		kemudian agar supaya bisa berjalan secara langsung, refresh environment dengan perintah
		"source /etc/environment" (lagi-lagi tanpa tanda petik)
		
#### Install Oh-My-Zsh on ubuntu 14.04 :
	- First of all, download zsh first with command "sudo apt-get install zsh"
	- Then "sudo apt-get install git", because it need download source from github
	- Then see https://github.com/robbyrussell/oh-my-zsh to Install (just the install)
	- And then run command "chsh -s `which zsh`"
	- Ok, now your Zsh is done, just need to change the theme, maybe to "agnoster" in "~/.zshrc"
	- If you getting font error, try
		cd ~/.oh-my-zsh/themes/
		git checkout d6a36b1 agnoster.zsh-theme
	 Or try installing the fonts (All font in >>, just try https://github.com/nmfzone/fonts)
		
#### How to Add New Webserver in NginX
	$ sudo mkdir -p /var/www/example.com/html
	$ sudo chown -R $USER:$USER /var/www/example.com/html
	$ sudo chmod -R 755 /var/www
	$ sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/example.com
	$ sudo nano /etc/nginx/sites-available/example.com
	$ sudo ln -s /etc/nginx/sites-available/example.com /etc/nginx/sites-enabled/
	$ sudo nano /etc/hosts (add new domain)
	
#### CHEATS SHEET *UNIX
	- tar -xvzf nama_file.tgz  => Extract .tgz
	- sudo su  => Masuk sebagai root (tapi sebaiknya jangan, lebih baik setiap jalankan command tambahkan sudo)
	- ls -la  => Melihat ini List directory
	- chmod -R 777 nama_folder / chmod 777 nama_file  => Merubah hak akses file
	- ln -s nama_folder_asal nama_folder_tujuan => Membuat symbolink Link
	- curl -sSL alamat  => Mendownload file menggunakan cURL
	- wget  => Mendownload file menggunakan wget
```

# Tutorial ElementaryOS
```

#### This to do after Installing Elementary OS :
	- Download exstra plugin to play .mp3/.mp4
		$ sudo apt-get install ubuntu-restricted-extras
	- Install NginX and MySQL
		$ sudo apt-get install nginx
		$ sudo apt-get install mysql-server mysql-client
	- Install PHP, NPM, NodeJs, git, composer
		PHP & Nginx : 
			$ sudo add-apt-repository ppa:ondrej/php5
			$ sudo apt-get install php5-fpm php5-cli php5-curl
		PHP Mcrypt (for Laravel or other) :
			$ sudo apt-get install mcrypt php5-mcrypt
			$ sudo php5enmod mcrypt
			$ sudo service nginx restart
		NPM : 
			$ sudo apt-get install npm
			$ sudo ln -s /usr/bin/nodejs /usr/bin/node (command : node / nodejs)
		Composer :
			$ curl -sS https://getcomposer.org/installer | php
			$ sudo mv composer.phar /usr/bin/composer
		Git : 
			$ sudo apt-get install git
	- Install Python and Pip
		$ sudo add-apt-repository ppa:fkrull/deadsnakes
		$ sudo apt-get install python3.3
		$ sudo apt-get install python3.4
		$ sudo apt-get install python-pip
	- Customize Terminal
		- Enable 256 color xterm :
			$ sudo apt-get install ncurses-term
			$ vim ~/.bashrc OR $ vim ~/.zshrc
			add export TERM="xterm-256color"
	- Install Java
		$ sudo add-apt-repository ppa:webupd8team/java
		$ sudo apt-get install oracle-java8-installer
		$ sudo apt-get install oracle-java8-set-default

#### Shortcut Keys
    Ctrl + T - Open a new tab in Files
    Ctrl + Alt + T – Starts terminal
    Alt + Tab - Switch between apps that are opened
    Superkay + A – Show all windows on every desktop
    Superkey + W – Show all windows on the current desktop
    Superkey + Tab – Switch between desktops (in order they are used)
    Superkey + directional arrows – Switch between desktops
    Superkey + 1,2,3,4,5 … – Switch between desktops

```

#### Laravel :
```
  location / {
        try_files $uri $uri/ /index.php?$query_string;
  }
```

#### Codeigniter :
```
  location / {
        try_files $uri $uri/ @ci_index;
  }
  
  location @ci_index{
	rewrite ^(.*) /index.php?$1 last;
  }
```

# Tutorial Android
#### ANDROID STUDIO
```
	- Error (android.support.v7.internal.widget.actionBarOverlay)
		http://stackoverflow.com/questions/29195195/android-studio-rendering-problems-classes-could-not-be-found
```
#### Install GoogleApps di GenyMotions
```
http://stackoverflow.com/questions/20121883/how-to-install-google-play-services-in-a-genymotion-vm-with-no-drag-and-drop-su
```

# Tutorial Website
```
http://www.youtube.com/attribution_link?a=WkXjCu-8U6w&u=%2Fwatch%3Fv%3DobrHov9XfRk%26feature%3Dshare
```
### Laravel
```
a
```
### Ruby on Rails
```
	https://gorails.com/setup/ubuntu/14.04
	
	- Install RVM (you must Install cURL first) :
		$ gpg --keyserver hkp://keys.gnupg.net --recv-keys
		$ \curl -L https://get.rvm.io | bash -s stable
		$ cd ~/.rvm/archieve
		$ tar -xvzf your_rvm_version.tgz
		$ cd your_rvm_version
		$ ./install
		$ source ~/.rvm/scripts/rvm
		$ rvm requirements
	- Add to your terminal (~/.bashrc or ~/.zshrc or ~/.bash_profile)
		export PATH="$PATH:$HOME/.rvm/bin" # Add RVM to PATH for scripting
		[[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm"
	- Install Ruby
		$ rvm install ruby or $ rvm install 2.2.2
		$ rvm use ruby --default (maybe will not work, you may use another way)
			$ rvm list (see your ruby version that have been installed)
			$ rvm alias create default ruby-2.2.2 (use ruby version 2.2.2 for default)
	- Install Gems
		$ rvm rubygems current
	- Install Rails
		$ gem install rails or $ gem install rails -v 4.2.1 (to install specific version)
		
	- Creating new Apps :
		Using MySql :
			$ rails new myapp -d mysql
			$ subl config/database.yml (edit database credentials)
			$ rake db:create
			$ rails server
		Using PostgreeSql :
			$ rails new myapp -d postgresql
			$ subl config/database.yml (edit database credentials)
			$ rake db:create
			$ rails server
```
### JavaScript
#### NodeJs
```
http://rizkylab.com/install-node-js-dan-mongodb-di-lubuntu-14-04/
http://rizkylab.com/deploy-node-js-on-heroku/
	- Install MongoDB (mongoose) untuk NodeJs :
		$ sudo npm install mongoose
```
#### AngularJs
```
c
```
#### EXTJs
```
http://rizkylab.com/membuat-crud-dengan-ext-js-4/
```
### Database
#### MongoDB
```
http://rizkylab.com/install-node-js-dan-mongodb-di-lubuntu-14-04/
	$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
	$ echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' | sudo tee /etc/apt/sources.list.d/mongodb.list
	$ sudo apt-get update
	$ sudo apt-get install mongodb-org mongodb-org-server
```
#### Postgree SQL
```
	$ sudo sh -c "echo 'deb http://apt.postgresql.org/pub/repos/apt/ precise-pgdg main' > /etc/apt/sources.list.d/pgdg.list"
	$ wget --quiet -O - http://apt.postgresql.org/pub/repos/apt/ACCC4CF8.asc | sudo apt-key add -
	$ sudo apt-get update
	$ sudo apt-get install postgresql-common
	$ sudo apt-get install postgresql-9.3 libpq-dev
	
	Untuk setup username dan Password :
	$ sudo -u postgres createuser your_username -s
	$ sudo -u postgres psql
	$ postgres=# \password your_username
```
### Next? 
```
d
```

# DesktopApps
### Java
```
test
```

# Tutorial WINDOWS
```
Menghilangkan dan atau menambah context menu (saat klik kanan) :
http://www.howtogeek.com/howto/windows-vista/add-any-application-to-the-desktop-right-click-menu-in-vista/
http://www.howtogeek.com/howto/windows-vista/how-to-clean-up-your-messy-windows-context-menu/
http://www.thewindowsclub.com/remove-click-context-menu-items-editors
```

# Fonts
####Woff to Ttf
```
https://andrewsun.com/services/woffer-convert-woff-fonts/
```

#Others
```
Share Localhost dengan ngrok : http://rizkylab.com/share-localhost-ke-public-menggunakan-ngrok/
```
