# colorization-project


## Install GPU environment 

### 

1- download cuda accourding to the machine specifications for our case 
```
wget https://developer.nvidia.com/compute/cuda/9.0/Prod/local_installers/cuda-repo-ubuntu1704-9-0-local_9.0.176-1_amd64-deb
```
2- Install cuda 
```
    `sudo dpkg -i cuda-repo-ubuntu1704-9-0-local_9.0.176-1_amd64.deb`
    `sudo apt-key add /var/cuda-repo-<version>/7fa2af80.pub`
    `sudo apt-get update`
    `sudo apt-get install cuda`

```

4- Add lines to bachrc 
```
   `echo 'export CUDA_HOME=/usr/local/cuda' >> ~/.bashrc`  
   `echo 'export PATH=$PATH:$CUDA_HOME/bin' >> ~/.bashrc`  
   `echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CUDA_HOME/lib64' >> ~/.bashrc`  
   `source ~/.bashrc`

```
3 - Download CUDNN library files from our drive using the commandline using the command mentioned below 
* https://drive.google.com/open?id=1hffslhDUX3G10J08kPJtcvm_e9eDvV0x
* https://drive.google.com/open?id=1SC7U_u1hhmeUP0YBJ-hpK6IejwxVGG7Z
* https://drive.google.com/open?id=1Lz3ADsM3wp2FF5QhPyLG1KnozFbzb2_v

4 - Install the three files the normal file then the dev then the doc in order like this

    `sudo dpkg -i libcudnn7_7.0.3.11-1+cuda9.0_amd64.deb`

5- Install the tensorflow normally using the following commands 
```
    `sudo apt-get install python3-pip python3-dev python-virtualenv`
    `virtualenv --system-site-packages -p python3 tensorflow`
    `pip3 install --upgrade tensorflow`
    `pip3 install --upgrade tensorflow-gpu`
```

6- Activate tensorflow and run whatever you want :)

    `source ~/tensorflow/bin/activate`
    
    
## general useful commads for the cloud and environment

### Downlaod from a file from the drive using the terminal

** replace {token} with file token and {FILENAME} with the file name 
```
wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id={token}' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id={token}" -O {FILENAME} && rm -rf /tmp/cookies.txt
```

### Upload/download from/to the cloud from/to the machine 
** follow this link to download, install and initialize gcloud
https://cloud.google.com/sdk/downloads

then to download from machine follow this command and reverse source with distination to upload a file to the gloud machine
```
 gcloud compute  copy-files {instanceName}:{full path of the file in the machine} {path of the distination desired on laptop}
```

### Unzip a file using terminal

```
 sudo apt-get install unzip
 unzip file.zip -d destination_folder
```

### Zip a file using terminal

```
 sudo apt-get install unzip
 unzip file.zip -d destination_folder
```
### Compress zip file

```
sudo apt-get install zip gzip tar
zip -r my_arch.zip my_folder

```
* For tar files 

* Compress
```
sudo apt-get install tar
tar -cvzf may_arch.tar.gz my_folder
```
* Extract
```
sudo apt-get install tar
tar -xvzf may_arch.tar.gz
```

