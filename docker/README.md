# Docker Setup
```
lsblk
sudo mkdir /mnt/MEDIA_DRIVE
sudo mount -o umask=0022,gid=1000,uid=1000 /dev/sda2 /mnt/MEDIA_DRIVE

sudo umount /mnt/MEDIA_DRIVE

sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
apt-cache policy docker-ce
sudo apt install docker-ce
sudo systemctl status docker
sudo usermod -aG docker ${USER}
su - ${USER}
groups
```

# Jellyfin
```
# start
docker compose -f jellyfin.dockerFile up -d
# stop
docker compose -f jellyfin.dockerFile down
```


