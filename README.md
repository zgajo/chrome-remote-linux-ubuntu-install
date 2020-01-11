# chrome-remote-linux-ubuntu-install

Instalation of chrome-remote on linux Ubuntu ( Last command had to be added ) as without that, after restart, boot into desktop won't work 

## INSTALATION

wget https://dl.google.com/linux/direct/chrome-remote-desktop_current_amd64.deb

sudo apt update

sudo apt install --assume-yes \
    --with-source=chrome-remote-desktop_current_amd64.deb \
    chrome-remote-desktop

sudo DEBIAN_FRONTEND=noninteractive \
    apt install --assume-yes xfce4 desktop-base


echo "xfce4-session" > ~/.chrome-remote-desktop-session

sudo apt install --assume-yes xscreensaver

sudo apt install --assume-yes task-xfce-desktop

sudo systemctl disable lightdm.service

wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

sudo apt install --assume-yes  google-chrome-stable \
    --with-source=google-chrome-stable_current_amd64.deb
    
sudo dpkg-reconfigure lightdm
