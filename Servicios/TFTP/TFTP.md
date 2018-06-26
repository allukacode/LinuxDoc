[root@centos /]# mkdir -p /tftpboot/netboot/
[root@centos /]# mount -o loop /home/guest/debian-live-9.4.0-amd64-gnome.iso /mnt/
[root@centos /]# mount /home/guest/debian-live-9.4.0-amd64-gnome.iso /var/ftp/debian9