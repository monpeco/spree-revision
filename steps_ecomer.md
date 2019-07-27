### repo
https://github.com/monpeco/spree-revision.git

### Update apt-get pakages 
$ sudo apt-get update

## Install rvm - https://github.com/rvm/ubuntu_rvm
### install software-properties-common
$ sudo apt-get install software-properties-common

### Add the PPA and install the package
$ sudo apt-add-repository -y ppa:rael-gc/rvm
$ sudo apt-get update
$ sudo apt-get install rvm

### Install ruby
$ rvm install 2.5

### Install Postgresql
#### Enable postgresql apt repository
$ sudo apt-get install wget ca-certificates
$ wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
$ sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'

#### Install postgres
$ sudo apt-get update
$ sudo apt-get install postgresql postgresql-contrib

### check that rubygem is install
$ which gem
$ gem update --system

### install bundler
$ gem install bundler

### install imageMagick
$ sudo apt install imageMagick

### install node
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs

### Install rails
$ gem install rails -v 5.2.1

### Install docker
$ sudo apt-get install docker.io

### Install pg gem
$ gem install pg

### Change to postgres
$ sudo -i -u postgres
$ psql 
# exit
$ exit
$ sudo -u postgres pqsl

### create a user (role in postgres)
# create role myapp with createdb login password 'password1';

### create rails app with postgres
$ rails new myapp --databse=postgresql

gem install pg -v '1.1.4' --source 'https://rubygems.org/'
bundle install

sudo chsh -s /bin/bash monpeco

https://stackoverflow.com/questions/18664074/getting-error-peer-authentication-failed-for-user-postgres-when-trying-to-ge
sudo service postgresql restart

sudo mount -t vboxsf VirtualBox

### Change the authentication from peer to md5
https://stackoverflow.com/questions/15306770/pg-peer-authentication-failed

### To take the changes in the authentication
/etc/init.d/postgresql reload

### To create the db
rake db:create
rake db:migrate

### install generetors
rails g spree:install --user_class=Spree::User
rails g spree:auth:install
rails g spree_gateway:install

### User in spree
Email [spree@example.com]: 
Password [spree123]: 

### Check versions
ruby --version
ruby 2.5.5p157 (2019-03-15 revision 67260) [i686-linux]
rails --version
Rails 5.2.3

