dotfiles
========

== Install thoughtbot's laptop
bash <(wget -qO- https://raw.githubusercontent.com/thoughtbot/laptop/master/linux)

== Clone repo
git clone git@github.com:simpl1g/dotfiles.git .
git submodule init
sudo apt-get install -y dconf-cli
./gnome-terminal-colors-solarized/install.sh

== Install Chrome

  wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb &&
	  sudo dpkg -i google-chrome-stable_current_amd64.deb &&
	  rm -f google-chrome-stable_current_amd64.deb
