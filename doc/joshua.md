# Joshua 
This is the documentation for Joshua, joshua is my laptop(T14) 

### OS
we use [linux mint xfce](https://linuxmint.com/download.php) but cinnamon will maybe also work

### hardware
the hardware of joshua is an thinkpad T14 with an added smart card slot for my smartcard(duh)

### setup 

1. download [the ISO](https://linuxmint.com/download.php)
2. run `sudo dd if=IMAGENAME.iso of=/dev/mmcblk0 bs=1M status=progress`
3. boot into this live usb and install linux mint
4. install `openssh-server` 


`
 and then run: 
`ansible-playbook -i hosts.ini tasks/joshua.yml`