dotfiles
========

== Install thoughtbot's laptop
bash <(wget -qO- https://raw.githubusercontent.com/thoughtbot/laptop/master/linux)

Generate ssh keys
=====

ssh-keygen -t rsa -C "konstantin@ilchenko.by"

Add to github


== Clone repo
git init
git remote add origin git@github.com:simpl1g/dotfiles.git
git fetch
git checkout -t origin/master
git clone git@github.com:Anthony25/gnome-terminal-colors-solarized.git
./gnome-terminal-colors-solarized/set_dark.sh

== Install Chrome

  wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb &&
	  sudo dpkg -i google-chrome-stable_current_amd64.deb &&
	  rm -f google-chrome-stable_current_amd64.deb
