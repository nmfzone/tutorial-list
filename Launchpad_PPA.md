# All About Launchpad PPA

##### Packaging
Example file name : try_this.tar.gz
1. `tar -xvzf try_this.tar.gz`
2. `cd try_this`
3. `dh_make -f ../try_this.tar.gz`

##### Building
Example package folder name : try_this
1. `cd try_this`
2. `debuild -S -k[Your_OpenPGP_Key]`

##### Upload
`dput ppa:username/ppa_name the_change_files.changes`


### Common errors :

##### gpg: no valid OpenPGP data found.
`gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv [THE_KEYS]`
