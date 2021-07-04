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

# Installing Ruby & Rails on Ubuntu
cd $HOME

sudo apt-get update

sudo apt install curl

curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -

curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -

echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt-get update

sudo apt-get install git-core zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev software-properties-common libffi-dev nodejs yarn

git clone https://github.com/rbenv/rbenv.git ~/.rbenv

echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc

echo 'eval "$(rbenv init -)"' >> ~/.bashrc

exec $SHELL

git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build

echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc

exec $SHELL

rbenv install 3.0.0

rbenv global 3.0.0

rbenv local 3.0.0

gem install bundler

rbenv rehash

gem install rails

bundle install
