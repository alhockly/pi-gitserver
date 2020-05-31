# pi-gitserver
git server on a pi with external disk

mkdir /gitRepos
install gogs - > https://pimylifeup.com/raspberry-pi-gogs/

in custom/app.ini

[repository.upload]

FILE_MAX_SIZE = 300




run to get drive details
lsblk -o "NAME,MAJ:MIN,RM,SIZE,RO,FSTYPE,MOUNTPOINT,UUID"

for user uid
id -u <username> 

for user gid
id -u <username> 

sudo nano /etc/fstab
add line
LABEL=<disk label> /gitRepos <FSTYPE> defaults,auto,uid=<uid of git user>,gid=<gid of git user>,users,rw,nofail 0 0



connect to ip address of pi port 3000
