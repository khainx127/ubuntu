Check disk usage:
```
df -h
```

Check server version:
```
uname -a
```
Create shortcut:
```
ln -s /home/khainguyen/projects /home/khainguyen/Desktop/
```
Install Nvidia driver:
```
sudo lshw -C display
apt search nvidia-driver
sudo apt install nvidia-driver-390
sudo reboot
nvidia-smi
```

Install ibus-unikey:
```
sudo apt-get install ibus-unikey
ibus restart
```
Open Settings -> Region & Language, add Vietnamese (Unikey) at Input Sources

Install Sound:
```
sudo apt remove --purge alsa-base alsa-utils pulseaudio pulseaudio-utils pavucontrol
sudo apt install pulseaudio pavucontrol
```

Install Rar:
```
sudo apt-get install unrar
unrar x file.rar
```

Install Git:
```
sudo apt install git
git config --global credential.helper store
```

Install Node:
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
nvm install 10.15.3
nvm install 12.18.2
nvm alias default v12.18.2
node --version
```

Install Yarn:
```
sudo apt install curl
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update && sudo apt install yarn
```

Install NetCore (Ubuntu 20.04)
```
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
sudo apt-get install -y apt-transport-https
sudo apt-get update && sudo apt-get install -y dotnet-sdk-3.1
sudo apt-get install -y dotnet-sdk-2.1
```
Install Docker:
```
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
docker --version
```
Install Docker Compose:
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
docker-compose -version
```
Run docker without sudo:
```
sudo gpasswd -a $USER docker
newgrp docker
```
Logout to activate changes

Fix error The configured user limit (128) on the number of inotify instances has been reached
```
echo fs.inotify.max_user_instances=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p
```

Install gnome secret lib
```
sudo apt install gnome-keyring
```
