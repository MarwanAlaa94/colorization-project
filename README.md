# colorization-project


## install GPU environment 

### 

1- download cuda accourding to the machine specifications for our case 
```
wget https://developer.nvidia.com/compute/cuda/9.0/Prod/local_installers/cuda-repo-ubuntu1704-9-0-local_9.0.176-1_amd64-deb
```
2- install cuda 
```
    `sudo dpkg -i cuda-repo-ubuntu1704-9-0-local_9.0.176-1_amd64.deb`
    `sudo apt-key add /var/cuda-repo-<version>/7fa2af80.pub`
    `sudo apt-get update`
    `sudo apt-get install cuda`

```
## general useful commads for the cloud and environment

### downlaod from a file from the drive using the terminal

** replace {token} with file token and {FILENAME} with the file name 
```
wget --load-cookies /tmp/cookies.txt "https://docs.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://docs.google.com/uc?export=download&id={token}' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id={token}" -O {FILENAME} && rm -rf /tmp/cookies.txt
```

### upload/download from/to the cloud from/to the machine 
** follow this link to download, install and initialize gcloud
https://cloud.google.com/sdk/downloads

then to download from machine follow this command and reverse source with distination to upload a file to the gloud machine
```
 gcloud compute  copy-files {instanceName}:{full path of the file in the machine} {path of the distination desired on laptop}
```

### unzip a file using terminal

```
 sudo apt-get install unzip
 unzip file.zip -d destination_folder
```

### zip a file using terminal

```
 sudo apt-get install unzip
 unzip file.zip -d destination_folder
```
### compress zip file

```
sudo apt-get install zip gzip tar
zip -r my_arch.zip my_folder

```
* for tar files 

* compress
```
sudo apt-get install tar
tar -cvzf may_arch.tar.gz my_folder
```
* extract
```
sudo apt-get install tar
tar -xvzf may_arch.tar.gz
```

