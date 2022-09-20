/home/pi/Software/bkup_rpimage/bkup_rpimage.sh start -cz -l -f /home/pi/SDBackups/PiBackup.img


https://github.com/lzkelley/bkup_rpimage


# Examples:

## Start backup to rpi_backup.img, creating it if it does not exist:

```
bkup_rpimage.sh start -c /path/to/rpi_backup.img
```

## Start backup to rpi_backup.img, creating it if it does not exist limiting the size to 8000Mb

```
bkup_rpimage.sh start -s 8000 -c /path/to/rpi_backup.img
```

## Use the RPi's hostname as the SD Image filename:

```
bkup_rpimage.sh start /path/to/$(uname -n).img
```

## Use the RPi's hostname and today's date as the SD Image filename, creating it if it does not exist, and compressing it after backup:

```
bkup_rpimage.sh start -cz /path/to/$(uname -n)-$(date +%Y-%m-%d).img
```

## Mount the RPi's SD Image in /mnt/rpi_image:

```
bkup_rpimage.sh mount /path/to/$(uname -n).img /mnt/rpi_image
```

## Unmount the SD Image from default mountdir (/mnt/raspi-2014-11-10.img/):

```
bkup_rpimage.sh umount /path/to/raspi-2014-11-10.img
```