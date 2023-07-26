# Donald 
this is the documentation for the master node called Donald. This node does the following things:
- PXE server 
- ssh tunnel for the intire house

### OS
we use [debian for Raspberry Pi](https://raspi.debian.net/tested-images/)

### hardware
We use the raspberry pi 4 stolen from my school as donald

### setup 
Sadly debian doesnt have python anymore so we have to build it from source
If you only want to setup donald run the following command.

1. download [the ISO](https://raspi.debian.net/tested-images/)
2. unpack the iso with `xz -xf {ISO}`
3. run `sudo dd if=20230612_raspi_4_bookworm.img of=/dev/mmcblk0 bs=1M status=progress`
4. on one of the partitions in `/sysconf.txt` add `root_authorized_key={YOUR_PUB_key}` 

5. run: `echo "deb http://ftp.debian.org/debian stable main contrib non-free" | tee /etc/apt/sources.list`
6. run `apt install python -y`

`
 and then run: 
`ansible-playbook -i hosts.ini tasks/donald.yml`