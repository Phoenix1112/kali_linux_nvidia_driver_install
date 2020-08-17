update linux and install linux headers

```
sudo apt-get update; sudo apt-get upgrade -y; sudo apt-get install linux-headers-$(uname -r)

```

Download Driver from Nvidia website

```
https://www.nvidia.com.tr/drivers
```

remove all nvidia drivers

```
sudo apt purge nvidia-*
```

install this settings

```
sudo apt install build-essential dkms
```

kali linux working with "nouveau" ... we will disable it..

```
echo -e "blacklist nouveau\noptions nouveau modeset=0\nalias nouveau off" > /etc/modprobe.d/blacklist-nouveau.conf
update-initramfs -u && reboot
```

when the computer starts it will remain on a black screen. Press ctrl + alt + f2 and switch to login page.
After logging in, let's go to the directory of the nvidia driver file. Let's run the nvidia driver now.

```
sudo chmod +x nvidia-driver-name.run
sudo ./nvdia-driver-name.run --dkms -s

```

After the installation is finished, if the login page with a visual interface does not open, you can enter by pressing ctrl + alt + f2.

