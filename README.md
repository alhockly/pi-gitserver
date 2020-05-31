# pi-gitserver
git server on a pi with external disk

mkdir /gitRepos
install gogs - > https://pimylifeup.com/raspberry-pi-gogs/




edit fstab 
sudo nano /etc/fstab
add line
LABEL=<disk label> /gitRepos <file system> defaults,auto,uid=<uid of git user>,gid=<gid of git user>,users,rw,nofail 0 0

connect to ip address of pi port 3000
