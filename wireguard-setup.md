# WIREGUARD-SETUP
## Install:
```
sudo apt install -y wireguard
```

<br>

## Client side
### Add config file to wireguard directory:
```
sudo cp </path/to/file.conf> /etc/wireguard/wg0.conf
```
### Activate connection with:
```
sudo wg-quick up wg0
```

<br>

## Server side (pivpn):
#### Create new device config file:
```
pivpn -a
```
Follow through the setup guide. After that the config file will be created in the "/home/$USER/configs/" directory.
