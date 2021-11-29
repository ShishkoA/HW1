# Homework

## 1)
ls /usr/share/man/man?/*config*
ls /usr/share/man/man[1,7]/*system*

## 2)
find /usr/share/man -type f -name *help*
sudo find /usr/share/man -type f -name "conf*"

To have opportunity to delete file and folders with additional parameters in find command.

Example find:
Remove all files from /tmp
find /tmp -type f -delete

## 3)
tail -2 /etc/fstab
head -7 /etc/yum.conf
```bash
[linux@localhost ~]$ cat /etc/fstab | wc -l
11
[linux@localhost ~]$ head -15 /etc/fstab

#
#/etc/fstab
#Created by anaconda on Thu Nov 25 10:35:32 2021
#
#Accessible filesystems, by reference, are maintained under '/dev/disk'
#See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
/dev/mapper/centos-root /                       xfs     defaults        0 0
UUID=2235a5c4-f0ee-432c-9c67-daa9f3fe813e /boot                   xfs     defaults        0 0
/dev/mapper/centos-swap swap                    swap    defaults        0 0
[linux@localhost ~]$
```

## 4)
touch file_name{1..3}.md
mv file_name1.{md,textdoc}
mv file_name2{.md,}
mv file_name3.md{,.latest}
mv file_name1.{textdoc,txt}

## 5)
cd ~
cd ../home/linux
cd /home/linux

## 6)
mkdir -p new in-process/tread{0..2} processed
touch new/data{00..99}
cp new/data{00..33} in-process/tread0
cp new/data{34..66} in-process/tread1
cp new/data{67..99} in-process/tread2

ls -R in-process

cp in-process/tread[?] processed

cp in-process/tread{0..2}/* processed

ls in-process processed

diff -q new processed
