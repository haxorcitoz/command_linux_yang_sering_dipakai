# command_linux_yang_sering_dipakai
* `sudo systemctl start` nama.service
* `sudo systemctl stop` nama.service
* `sudo systemctl status` nama.service
* `sudo systemctl restart` nama.service
* `sudo systemctl daemon-reload`
* `sudo service cron reload` atau `/etc/init.d/cron reload` untuk reload crontab
* `kill -9` PID
* `screen -XS sessions_id quit` kill screen
* `sudo apt install wavemon` monitoring signal wifi via terminal
* `ps aux | grep` process-yang _dicari
* `sudo nano /etc/systemd/system/` nama.service
* `screen -d` untuk detach screen
* `sudo nano /etc/dhcpcd.conf`
* `sudo nano /boot/config.txt`
* [GPG key depreciation](https://askubuntu.com/questions/1407632/key-is-stored-in-legacy-trusted-gpg-keyring-etc-apt-trusted-gpg)
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
* [Membuat daemon service](https://www.linuxsec.org/2020/11/membuat-daemon-process-dengan-systemd.html)
* [Mengirim email menggunakan python](https://myhydropi.com/send-email-with-a-raspberry-pi-and-python/)
* [Mengganti nama wireless adapter](https://askubuntu.com/questions/1303099/how-to-change-the-name-of-wireless-interface)
* VNC server
  1. Install VNC server `sudo apt install tightvncserver`
  2. Jalankan VNC server dengan command `vncserver :1`
  3. Setting seperlunya
  4. Buat autostart dengan cara mengedit file rc.local dengan command `sudo nano /etc/rc.local`
  5. Tambahkan perintah `su - nama_user -c '/usr/bin/vncserver'` sebelum `exit 0`
  6. Restart
* [Membuat user baru di Debian](https://www.cloudpanel.io/tutorial/how-to-add-user-to-sudoers-in-debian/)
* [Mengganti password user di Debian](https://nordpass.com/blog/how-to-change-password-linux/)
* nmcli wifi
  1. `nmcli dev status` cek device status
  2. `nmcli radio wifi` cek status wifi enable atau disable, untuk enable pakai `nmcli radio wifi on`
  3. `nmcli dev wifi list` cek access point yang ada
  4. `sudo nmcli dev wifi connect network-ssid` konek ke open wifi
  5. `sudo nmcli dev wifi connect network-ssid password "network-password"` konek ke wpa2 wifi
  6. `sudo nmcli dev wifi connect network-ssid password "network-password" ifname wlan??` konek ke wpa2 dengan specified wireless interface
  7. Untuk disconnect cek dahulu device status dengan command `nmcli dev status` kemudian gunakan command `nmcli con down id connection_name`
  8. Untuk forget cek dahulu device status dengan command `nmcli dev status` kemudian gunakan command `nmcli connection delete CONNECTION_NAME`
* [Wifi Hotspot](http://www.orangepi.org/orangepiwiki/index.php/AP6275P_PCIe_NIC_creates_WIFI_hotspot_via_create_ap)
* [The following packages have been kept back](https://itsfoss.com/following-packages-have-been-kept-back/)
