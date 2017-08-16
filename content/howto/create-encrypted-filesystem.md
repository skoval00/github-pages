Title: Create encrypted LUKS filesystem
Date: 2017-08-16 18:20

[Cryptsetup FAQ](https://gitlab.com/cryptsetup/cryptsetup/wikis/FrequentlyAskedQuestions)

`cryptsetup luksOpen /dev/sdbX sdbX_crypt`
`mke2fs -j -L <volume-name> -t ext4 /dev/mapper/sdbX_crypt`
`mount /dev/mapper/sdb1_crypt /mnt`

Find device UUID with `lsblk` or `blkid`.

Add entry to /etc/crypttab
echo "sdX1_crypt UUID=<device-uuid> none luks" >> /etc/crypttab

Add /dev/mapper/sdX1_crypt to /etc/fstab
