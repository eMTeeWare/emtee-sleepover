# emtee-sleepover
A project to setup a bed-time focused, Raspberry Pi Zero based podcast player.

## Install OS
https://www.raspberrypi.org/downloads/
I use Raspberry Pi OS Lite (32 bit)

## Enable SSH
Place a file called `ssh` in the boot partition. The content does not matter.

## Enable Wi-Fi
Place a file callet `wpa_supplicant.conf` with the following content in the boot partition:
```conf
country=DE 
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev 
update_config=1 
network={
     ssid="WLAN SSID"
     scan_ssid=1
     psk="WLAN PASSWORT"
     key_mgmt=WPA-PSK
}
```
(Thanks to https://www.dahlen.org/2017/10/raspberry-pi-zero-w-headless-setup/)
