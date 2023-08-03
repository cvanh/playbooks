# lxd
this is the playland of lxd where we can prebuild and test our images

## inserting ssh keys
1. sudo apt install libguestfs-tools

## configuring host's dns resolver to also use lxd
because typing out ip addresses is hard you want to link the host's dns resolver to lxd.
you can do this by the following steps:

first find the inet addres of lxdbr0 by running: `ip addr show lxdbr0` in my case it was 10.89.0.1/16

now edit `/etc/dnsmasq.conf` to include this line
```server=/lxd/10.89.0.1```
because we changed our dnsmasq settings we need to reload it
`sudo systemctl reload dnsmasq`