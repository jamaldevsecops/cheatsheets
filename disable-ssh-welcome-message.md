# Disable SSH Welcome Message  
Ref: https://ubuntushell.com/disable-ssh-welcome-message/

To suppress a welcome message, begin by opening your terminal and modifying the /etc/ssh/sshd_config file with your preferred text editor.
```
sudo vim /etc/ssh/sshd_config
```
Once the file is opened, find the ```PrintMotd``` field and set its value to ```no```.
```
PrintMotd no
```
Save and close the file, then proceed to edit the /etc/pam.d/sshd file.
```
sudo vim /etc/pam.d/sshd
```
Comment them down by placing # in front of each line, as shown:
```
# session    optional     pam_motd.so  motd=/run/motd.dynamic
# session    optional     pam_motd.so noupdate
```
Save and close the file, restart your SSH server by running the following command:
```
sudo systemctl restart ssh
```
