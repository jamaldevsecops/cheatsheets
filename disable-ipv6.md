# Disable IPv6 on Ubuntu 20.04
### 1. Disable IPv6 Using GRUB
```
sudo nano /etc/default/grub
```
```
GRUB_CMDLINE_LINUX="ipv6.disable=1"
```
```
sudo update-grub
```
### 2. Reboot the System
```
sudo reboot
```
### 3. Verification
```
grep -Pqs '^\h*0\b' /sys/module/ipv6/parameters/disable && echo -e "\n -IPv6 is enabled\n" || echo -e "\n - IPv6 is not enabled\n"
```
