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
docker compose up -d
# stop
docker compose down
```

# Resources
https://www.youtube.com/watch?v=yMmxw-DZ5Ec
https://medium.com/@fabrice_/setting-up-a-media-server-jellyfin-and-making-it-securely-accessible-from-anywhere-in-the-world-ca3b4d9dd19e