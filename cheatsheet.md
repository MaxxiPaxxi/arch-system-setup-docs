# Linux Cheatsheet

## Docker Maintenance

Remove dangling images:

```sh
docker image prune
```

Remove all images not used by existing containers:

```sh
docker image prune -a
```

Remove stopped containers:

```sh
docker container prune
```

Remove all unused volumes:

```sh
docker volume prune
```

System prune:

```she
docker system prune
```

## Package Maintenance

Delete all cached versions of installed and uninstalled packages, except for the most recent (3 by default):

```sh
paccache -r
``` 

Clear out all cached packages that ar enot currently installed

```sh
pacman -Sc
```

Clear out all cached packages:

```sh
pacman -Scc
```


## Network Connections

Find connection interfaces:

`ip link`

Bring a connection interface up:

`ip link set dev {interface} up`

Configure:

`dchpcd`

Use netctl to view and control network connections:

`netctl list`

`netctl start {connection}`


## SSH

Create SSH Key for email address: 

`$ ssh-keygen -t rsa -b 4096 -C "email@address.com"`

Basic SSH key gen:

`$ ssh-keygen -t rsa`


## VPN

Run localhost VPN to server:

`$ ssh -L 3128:localhost:8888 -N root@111.111.111.11`

or:

`$ ssh -L 3128:localhost:8888 -N -i ~/.ssh/key_rsa root@111.111.111.11`

Command format:

`$ ssh -L {port}:{localhost} -N -i {/path/to/key.rsa} {user}@{host}`


To get this to work, change network settings to use localhost (port 3128) as the proxy.


## Mounting

To mount an ISO onto a USB drive:

`$ dd bs=4M if=/path/to/file.iso of=/dev/sdx status=progress && sync`


## Displays

```bash
xrandr --output HDMI-2 --auto --right-of eDP-1
```

```bash
~/.config/bspwm/bspwmrc
```


# Audio

```bash
aplay -l output
```
