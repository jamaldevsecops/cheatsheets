1. Open the suders file with root user. 
```
visudo
```
2. Apend the the following lines into the mentioned file. Don't forget to replace the 'user_name'.  
```
Cmnd_Alias DISABLE_SU = /bin/su
user_name ALL=(ALL) NOPASSWD: ALL, !DISABLE_SU
```
