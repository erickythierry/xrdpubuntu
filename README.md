# install GUI XFCE4 on ubuntu 18.04 server (VPS)

## connect to your VPS and run this comands bellow, one by one

> apt update

> apt install -y xubuntu-core^ xrdp xfce4 xfce4-goodies xorg dbus-x11
> x11-xserver-utils python3 python3-pip zip git ffmpeg
> thunar-archive-plugin

> sudo sed -i.bak '/fi/a #xrdp multiple users configuration \n
> xfce-session \n' /etc/xrdp/startwm.sh

> sudo ufw allow 3389/tcp

> sudo /etc/init.d/xrdp restart

> sudo reboot
