# command_linux_yang_sering_dipakai
* `sudo systemctl start` nama.service
* `sudo systemctl stop` nama.service
* `sudo systemctl status` nama.service
* `sudo systemctl restart` nama.service
* `sudo systemctl daemon-reload`
* `kill -9` PID
* `ps aux | grep` process-yang _dicari
* `sudo nano /etc/systemd/system/` nama.service
* `screen -d` untuk detach screen
* `sudo nano /etc/dhcpcd.conf`
* `sudo nano /boot/config.txt`
* [Slow Chromium](https://forums.raspberrypi.com/viewtopic.php?t=332018)
* [Github Syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [Using Nano](https://kb.iu.edu/d/aeug#:~:text=To%20delete%20the%20character%20highlighted,line%2C%20press%20Ctrl%2Dk%20.)
* [Set static ip](https://medium.com/digital-software-architecture/raspberry-pi-headless-configuration-ac0a3a31d184)
* [Shrink Pi Backup Image](https://github.com/Drewsif/PiShrink)
  1. `lsblk`
  2. `sudo mkdir /dev/myusb`
  3. `sudo mount /dev/sda1 /dev/myusb` sda1 adalah usb di `lsblk`
  4. `sudo dd if=/dev/mmcblk0 of=/dev/myusb/pibackupimg.img bs=1M status=progress`
  5. `cd /dev/myusb`
  6. `sudo pishrink.sh -z pibackupimg.img`
* Agar script bisa dijalankan langsung via terminal, pindahkan ke `/usr/local/bin`
* [Rpi Access Point](https://www.tomshardware.com/how-to/raspberry-pi-access-point)
