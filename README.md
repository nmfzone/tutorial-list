# tutorial-list
Merupakan tutorial-tutorial yang pernah saya gunakan

```
Cara Menulis di GitHub : https://help.github.com/articles/markdown-basics/
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

Install Vagrant di Ubuntu :
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

Setting Environment di Ubuntu :
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
b
```
### JavaScript
#### NodeJs
```
http://rizkylab.com/install-node-js-dan-mongodb-di-lubuntu-14-04/
http://rizkylab.com/deploy-node-js-on-heroku/
```
#### AngularJs
```
c
```
#### EXTJs
```
http://rizkylab.com/membuat-crud-dengan-ext-js-4/
```
### MongoDB
```
http://rizkylab.com/install-node-js-dan-mongodb-di-lubuntu-14-04/
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

# Fonts
####Woff to Ttf
```
https://andrewsun.com/services/woffer-convert-woff-fonts/
```

#Others
```
Share Localhost dengan ngrok : http://rizkylab.com/share-localhost-ke-public-menggunakan-ngrok/
```
