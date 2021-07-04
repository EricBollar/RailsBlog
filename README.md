# Creating a Blog with Ruby & Rails
# Steps Taken: https://guides.rubyonrails.org/getting_started.html
# Installing Ruby & Rails
brew update
brew install rbenv ruby-build
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zprofile echo 'eval "$(rbenv init -)"' >> ~/.zprofile
rbenv install -l
rbenv install 3.0.0
rbenv global 3.0.0
rbenv rehash
gem update --system 
** If Gem Update Does Not Work **
sudo gem install -n /usr/local/bin gemName 
** On Mac must log out and log back in for rehash to work **
gem install rails
