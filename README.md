# Creating a Blog with Ruby & Rails
# Steps Taken: https://guides.rubyonrails.org/getting_started.html
# Installing Ruby & Rails on Mac
brew update

brew install rbenv ruby-build

echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile echo 'eval "$(rbenv init -)"' >> ~/.bash_profile

echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zprofile echo 'eval "$(rbenv init -)"' >> ~/.zprofile

rbenv install -l

rbenv install 3.0.0

rbenv global 3.0.0

rbenv local 3.0.0

rbenv rehash

gem update --system 

** If Gem Update Does Not Work **

sudo gem install -n /usr/local/bin gemName 

** On Mac must log out and log back in for rehash to work **

gem install rails

# Installing Ruby & Rails on Ubuntu AWS instance
** SSH into Instance **

sudo apt-get update

sudo apt-get install curl

\curl -L https://get.rvm.io | bash -s stable --ruby

** If above cmd doesn't work, read message and combine keys with 2 commands below as site is deprecated **

sudo apt-get install gpgv2

gpg --keyserver keyserver.ubuntu.com --recv-keys KEYONE KEYTWO

source /home/ubuntu/.rvm/scripts/rvm

rvm get stable --autolibs=enable

rvm install ruby

** Check Ruby and Sqlite3 worked **

ruby -v

sqlite3 --version

curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -

sudo apt-get install -y nodejs

gem install rails

** Check Rails worked **

rails -v

bundle install

** Make sure to use db:migrate before starting rails server **

** To test if worked use: **

rails s -b 0.0.0.0

** If Error: Are you trying to open an SSL connection to a non-SSL Puma? **

Clear Cache or Switch Browser

** If Error: webpacker::Manifest::MissingEntryError in Articles#index **

sudo apt install npm

sudo npm install --global yarn

yarn remove @rails/webpacker

rm -rf ./node_modules

yarn add @rails/webpacker@^5.2.1

** To run rails server indefinitely: **

rails s -d -b 0.0.0.0
