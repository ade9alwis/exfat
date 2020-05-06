[root@Serv2020 ~]# wget https://github.com/ade9alwis/exfat/blob/master/nux-dextop-release-0-1.el7.nux.noarch.rpm 

[root@Serv2020 ~]# md5sum nux-dextop-release-0-1.el7.nux.noarch.rpm

b7f21c723bbee047d3be5dd7ca0e3161  nux-dextop-release-0-1.el7.nux.noarch.rpm

[root@Serv2020 ~]# sha1sum nux-dextop-release-0-1.el7.nux.noarch.rpm

[root@Serv2020 ~]# yum install  nux-dextop-release-0-1.el7.nux.noarch.rpm

[root@Serv2020 ~]# yum install exfat-utils fuse-exfat

[root@Serv2020 ~]# lsblk -f
NAME        FSTYPE      LABEL          UUID                                   MOUNTPOINT
sda
├─sda1      ext4                       ca323c16-7e83-4be9-b606-41af0ad8e29f   /boot
└─sda2      LVM2_member                fJpnn4-YDqf-Y25Y-cuSt-CUEU-S7IT-RCm1Jl
  ├─cl-root xfs                        76fdcca1-b2f5-4c3b-a42c-29c40342e383   /
  └─cl-swap swap                       affd8701-a845-42a2-8ca5-eb08f96c6647   [SWAP]
sdb
└─sdb1      exfat                      76E8-CACF
sr0         iso9660     VBox_GAs_6.1.6 2020-04-09-18-00-17-30                 /run/media/alwis/Vbox_Gas_6.1.6

[root@Serv2020 ~]# mount /dev/sdb1 /mnt/

FUSE exfat 1.2.7

WARN: volume was not unmounted cleanly.
