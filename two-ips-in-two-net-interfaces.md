```
cp /etc/netplan/00-installer-config.yaml  /etc/netplan/01-installer-config.yaml
```
```
cat /etc/netplan/00-installer-config.yaml
```
```
network:
  version: 2
  renderer: networkd
  ethernets:
    ens32:
      addresses:
        - 192.168.10.21/24
      gateway4: 192.168.10.1
      nameservers:
        addresses: [8.8.8.8]
```
```
cat /etc/netplan/01-installer-config.yaml
```
```
network:
  version: 2
  renderer: networkd
  ethernets:
    ens34:
      addresses:
        - 192.168.11.21/24
      #gateway4: 192.168.11.1
      nameservers:
        addresses: [8.8.4.4]
```
```
netplan apply
```
