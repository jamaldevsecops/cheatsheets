1 Get anaconda : 
```
wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh
```
2. Install with bash:
```
chmod 700 Anaconda3-2022.05-Linux-x86_64.sh
```
```
./Anaconda3-2022.05-Linux-x86_64.sh
```
[type yes when asked for conda init]

3. Re-login to terminal
4. Create an environment:
```
conda create -n newenv python=3.10 [newenv can be named anything]
```
6. Activate the environment:
```
conda activate newenv
```
7.  Deactivate the environment:
```
conda deactivate
```
#-------------------------------End------------------------------

Check the virtual environment information. 
```
su - apsiscrm
conda info --envs
```
