# Repo
https://github.com/monpeco/spree-revision.git

# Update apt-get pakages 
```
$ sudo apt-get update
```

# Install ruby from rvm - https://github.com/rvm/ubuntu_rvm
#### 1. install software-properties-common
```
$ sudo apt-get install software-properties-common
```

#### 2. Add the PPA and install the package
```
$ sudo apt-add-repository -y ppa:rael-gc/rvm
$ sudo apt-get update
$ sudo apt-get install rvm
```

#### 3. Install ruby
```
$ rvm install 2.5
```

# Install Postgresql
#### 1. Enable postgresql apt repository
```
$ sudo apt-get install wget ca-certificates
$ wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
$ sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'
```

#### 2. Install postgres
```
$ sudo apt-get update
$ sudo apt-get install postgresql postgresql-contrib
```
# Check that rubygem is install
```
$ which gem
$ gem update --system
```
# Install bundler
```
$ gem install bundler
```

# Install imageMagick
```
$ sudo apt install imageMagick
```

# Install rails from node
#### 1. Install node
```
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
```

#### 2. Install rails
```
$ gem install rails -v 5.2.1
```

# Install docker
```
$ sudo apt-get install docker.io
```

# Postgres
#### 1. Install pg gem
```
$ gem install pg
```

#### 2. Change to postgres
```
$ sudo -i -u postgres
$ psql 
# exit
$ exit
$ sudo -u postgres pqsl
```

#### 3. Create a user (role in postgres)
```
# create role myapp with createdb login password 'password1';
```

#### 4. Create rails app with postgres
```
$ rails new myapp --databse=postgresql
```

#### 5. Install specific version of pg
```
$ gem install pg -v '1.1.4' --source 'https://rubygems.org/'
bundle install
```

#### 6.1 Error peer authentication
https://stackoverflow.com/questions/18664074/getting-error-peer-authentication-failed-for-user-postgres-when-trying-to-ge


#### 6.2 Change the authentication from peer to md5
https://stackoverflow.com/questions/15306770/pg-peer-authentication-failed

#### 7. To take changes in postgres
```
sudo service postgresql restart
```

#### 8. To take the changes in the authentication
```
/etc/init.d/postgresql reload
```

#### 9. To create the db
```
rake db:create
rake db:migrate
```

# Install Spree generetors
```
rails g spree:install --user_class=Spree::User
rails g spree:auth:install
rails g spree_gateway:install
```

#### 1. User in spree
```
Email [spree@example.com]: 
Password [spree123]: 
```

# Check versions
```
$ ruby --version
ruby 2.5.5p157 (2019-03-15 revision 67260) [i686-linux]
```
```rails --version
Rails 5.2.3
```

# Change shell to bash
```
sudo chsh -s /bin/bash monpeco
```

# Mount shared folder
```
sudo mount -t vboxsf VirtualBox
```

# Install vscode
```
sudo dpkg -i code_1.35.1-1560349847_i386.deb
```