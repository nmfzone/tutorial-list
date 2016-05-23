# All About Launchpad PPA

##### Packaging
Example file name : try_this.tar.gz<br>
1. `tar -xvzf try_this.tar.gz`<br>
2. `cd try_this`<br>
3. `dh_make -f ../try_this.tar.gz`<br>

##### Building
Example package folder name : try_this<br>
1. `cd try_this`<br>
2. `debuild -S -k[Your_OpenPGP_Key]`<br>

##### Upload
`dput ppa:username/ppa_name the_change_files.changes`


### Common errors :

##### gpg: no valid OpenPGP data found.
`gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv [THE_KEYS]`
