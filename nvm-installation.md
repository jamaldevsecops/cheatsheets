Source: https://www.digitalocean.com/community/tutorials/nodejs-node-version-manager
	  https://github.com/nvm-sh/nvm


1. Install Node Version Manager (NVM)
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```
or
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```
2. Once installed, close and reopen your terminal application for changes to take effect or run the following.
```
source .bashrc
```
3. Install Multiple Nodejs Version
```
nvm install 16.13.2
```
```
nvm install 14
```
4. Listing Installed Node.js Versions
```
nvm ls
``` 
5. The default version of Node is the version that will be available when you open a new shell.
```
node -v
```
6. Set 16.13.2 as your system default version.
```
nvm alias default 16.13.2
```
7. Open new terminal and set Node 17 is default version for this terminal. 
```
nvm use 
node -v
```
7. Open another new terminal and set Node 14 is default version for this terminal. 
```
nvm use 14
node -v
```
8. Allow apsisdev user to swich node version. 

Install NVM with outher user
=========================================
login with the user
create a directory namely .nvm
all other procedures are same

9. Upgrade or Install Specfic Version of NPM: 
```
npm --version
npm install -g uuid@latest
npm install -g npm@latest 
```
9. Install pm2
```
npm install -g pm2@latest
```
10. Install Yarn
```
npm install -g yarn@latest
```



