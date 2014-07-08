dotfiles
========

== Install thoughtbot's laptop
bash <(wget -qO- https://raw.githubusercontent.com/thoughtbot/laptop/master/linux)

curl -L http://install.ohmyz.sh | sh

Generate ssh keys
=====

ssh-keygen -t rsa -C "konstantin@ilchenko.by"

Add to github


== Clone repo
git init
git remote add origin git@github.com:simpl1g/dotfiles.git
git fetch
rm .bashrc
rm .zshrc
git checkout -t origin/master
git clone git@github.com:Anthony25/gnome-terminal-colors-solarized.git
./gnome-terminal-colors-solarized/set_dark.sh

== Install Chrome

  wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb &&
	  sudo dpkg -i google-chrome-stable_current_amd64.deb &&
	  rm -f google-chrome-stable_current_amd64.deb

sudo apt-get install -y ubuntu-restricted-extras nautilus-dropbox libappindicator1 unity-tweak-tool gnome-tweak-tool

gsettings set com.canonical.Unity.Lenses disabled-scopes "['more_suggestions-amazon.scope', 'more_suggestions-u1ms.scope', 'more_suggestions-populartracks.scope', 'music-musicstore.scope', 'more_suggestions-ebay.scope', 'more_suggestions-ubuntushop.scope', 'more_suggestions-skimlinks.scope']"

sudo add-apt-repository -y ppa:videolan/stable-daily
sudo add-apt-repository -y ppa:otto-kesselgulasch/gimp
sudo add-apt-repository -y ppa:gnome3-team/gnome3
sudo add-apt-repository -y ppa:webupd8team/java
sudo add-apt-repository -y ppa:webupd8team/y-ppa-manager
sudo add-apt-repository -y ppa:webupd8team/sublime-text-3

echo 'deb http://download.videolan.org/pub/debian/stable/ /' | sudo tee -a /etc/apt/sources.list.d/libdvdcss.list &&
echo 'deb-src http://download.videolan.org/pub/debian/stable/ /' | sudo tee -a /etc/apt/sources.list.d/libdvdcss.list &&
wget -O - http://download.videolan.org/pub/debian/videolan-apt.asc|sudo apt-key add -

sudo apt-get update
sudo apt-get -y upgrade
sudo apt-get -y dist-upgrade

sudo apt-get install -y synaptic vlc gimp gimp-data gimp-plugin-registry gimp-data-extras y-ppa-manager bleachbit openjdk-7-jre oracle-java8-installer flashplugin-installer unace unrar zip unzip p7zip-full p7zip-rar sharutils rar uudeview mpack arj cabextract file-roller libxine1-ffmpeg mencoder flac faac faad sox ffmpeg2theora libmpeg2-4 uudeview libmpeg3-1 mpeg3-utils mpegdemux liba52-dev mpeg2dec vorbis-tools id3v2 mpg321 mpg123 libflac++6 totem-mozilla icedax lame libmad0 libjpeg-progs libdvdcss2 libdvdread4 libdvdnav4 libswscale-extra-2 ubuntu-restricted-extras ubuntu-wallpapers* sublime-text-installer krusader
Install Skype 4.3
====

sudo apt-get purge skype skype-bin:i386 skype:i386 ; sudo apt-get install sni-qt:i386 ; wget http://www.skype.com/go/getskype-linux-beta-ubuntu-64 -O /tmp/skype-ubuntu-latest_i386.deb && sudo dpkg -i /tmp/skype-ubuntu-latest_i386.deb ; sudo apt-get install -f

Finish
====

sudo apt-get -f install &&
sudo apt-get autoremove &&
sudo apt-get -y autoclean &&
sudo apt-get -y clean
