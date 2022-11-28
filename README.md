# Contabo-install-GUI

https://www.youtube.com/watch?v=_NnxgAQsJkE&t=855s

adduser NEWUSER   (password : e.g paste  se7ye8pc5hs0  )

usermod -aG sudo,adm NEWUSER && su NEWUSER

sudo apt-get update && sudo apt-get upgrade -y

sudo apt-get install ubuntu-desktop mmv htop stacer gnome-software xrdp -y

sudo rm /usr/share/polkit-1/actions/org.freedesktop.color.policy

sudo sed -i 's/3389/53579/g' /etc/xrdp/xrdp.ini

sudo sed -i 's/#Port 22/Port 53572/g' /etc/ssh/sshd_config

sudo ufw allow 53572 && sudo ufw allow 53579 && sudo ufw enable && sudo ufw status numbered


sudo reboot   


#Firewall Settings
https://ubuntu.com/server/docs/security-firewall

sudo ufw enable

sudo ufw allow 22

