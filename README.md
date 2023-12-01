# Mapping-between-Linux-and-MacOs-To-Run-DMOJ

This is Linux commands to run on Ubuntu of DMOJ 
See their instruction to run its font-end : [https://docs.dmoj.ca/#/site/installation](https://docs.dmoj.ca/#/site/installation)

This is a mapping, I convert to MacOs (remember to install Brew) :

First Of All,run this command to install Brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"


Installing the prerequisites
$ brew update
$ brew install git gcc make python3 libxml2 libxslt zlib gettext curl redis
$ brew services start redis
$ brew install node@18
$ export LDFLAGS="-L/usr/local/opt/node@18/lib"  
$ export CPPFLAGS="-I/usr/local/opt/node@18/include"
$ sudo  npm install -g sass postcss-cli postcss autoprefixer

Create database
$ brew update
$ brew install mariadb
$ brew services start mariadb
$ brew install mysql-client
$ echo 'export PATH="/usr/local/opt/mysql-client/bin:$PATH"' >> ~/.zshrc
$ export LDFLAGS="-L/usr/local/opt/mysql-client/lib"
$ export CPPFLAGS="-I/usr/local/opt/mysql-client/include"
Installing prerequisites
$ python3 -m venv dmojsite
$ . dmojsite/bin/activate

(dmojsite) $ git clone https://github.com/DMOJ/site.git
(dmojsite) $ cd site
(dmojsite) $ git submodule init
(dmojsite) $ git submodule update
(dmojsite) $ pip3 install -r requirements.txt
(dmojsite) $ brew install pkg-config 
(dmojsite) $ export LDFLAGS="-L/usr/local/opt/openssl/lib"
(dmojsite) $ export CPPFLAGS="-I/usr/local/opt/openssl/include"
(dmojsite) $ pip3 install mysqlclient

Setting up Celery
$ brew services start redis

