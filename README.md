# tutorial-list
Merupakan tutorial-tutorial yang pernah saya gunakan

```
Cara Menulis di GitHub : https://help.github.com/articles/markdown-basics/
Cara Remote Github dengan Command Line :
 - git init
 - git add answer //disini answer merupakan folder yg ingin di upload
 - git commit -m "First Commit" //Ini untuk commit file ke repo lokal
 - git remote add origin https://github.com/nmfzone/yourproject.git //project yg akan di remote
 - git push -u origin master //ini untuk submit repo lokal ke repo inline github

Apabila ada file di repo github yg tidak ada di repo lokal :
 - git pull https://github.com/nmfzone/yourproject.git

Merubah/Menambah repo github :
 - git remote set-url origin git@github.com:username/projectname.git
 
Menghapus remote repo git :
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

http://www.unixmen.com/install-lemp-server-nginx-mysql-mariadb-php-phpmyadmin-ubuntu-14-1014-0413-10/

http://blog.andzhar.com/2014/11/12/125234/hhvm-nginx-di-ubuntu-server-14-04/

http://blog.andzhar.com/2014/12/11/152615/instalasi-composer-di-hhvm/

http://culttt.com/2013/06/17/setting-up-vagrant-with-laravel-4/

https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-virtual-hosts-server-blocks-on-ubuntu-12-04-lts--3

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
http://www.youtube.com/attribution_link?a=WkXjCu-8U6w&u=%2Fwatch%3Fv%3DobrHov9XfRk%26feature%3Dshare
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
