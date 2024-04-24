1. Pull the required docker images. 
```
docker pull pihole/pihole:latest
```
2. Disable the default dns resolver. 
```
sudo systemctl stop systemd-resolved
sudo systemctl disable systemd-resolved
```
3. Create the docker-compose file and past the following conents.
```
vim docker-compose.yml
```
```
version: "3"
services:
  pihole:
    container_name: pihole
    hostname: apsis.local
    image: pihole/pihole:latest
    ports:
      - "53:53/tcp"
      - "53:53/udp"
      - "8080:80/tcp"
    environment:
      TZ: "Asia/Dhaka"
      PIHOLE_DNS_: "8.8.8.8;8.8.4.4"
      WEBPASSWORD: "13F&b%2024"
      DNSSEC: "true"
      IPv6: "false"
      WEBTHEME: "default-dark"  
      
    volumes:
      - "./etc-pihole:/etc/pihole"
      - "./etc-dnsmasq.d:/etc/dnsmasq.d"
    restart: always
    
    networks:
      - pihole-net

networks:
  pihole-net:
```
4. Run the docker-compose file.
```
docker-compose up -d
