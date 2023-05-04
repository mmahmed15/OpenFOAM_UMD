A specific version of OpenFOAM-4.x used by Dr. Arnaud Trouve's group at UMD group for development of fire models

# Installation instructions
Below are steps to compile the OpenFoam-4.x version that supports Gcc-8.1 or older

## For Ubuntu 18.04.6
1. Update your system and install the following packages
```
sudo apt-get update
```
```
sudo apt-get upgrade
```
```
sudo apt-get install build-essential cmake git ca-certificates
```
```
sudo apt-get install flex libfl-dev bison zlib1g-dev libboost-system-dev libboost-thread-dev libopenmpi-dev openmpi-bin gnuplot libreadline-dev libncurses-dev libxt-dev
```
```
sudo apt-get install unzip zip
```


2. Download the source files in your home directory
```
cd ~
git clone https://github.com/mmahmed15/OpenFOAM_UMD.git
```

3. Navigate to the compile directory and unzip the source files
```
cd OpenFOAM_UMD
unzip ThirdParty-dev.zip
unzip OpenFOAM-dev.zip
```

4. Setting the environment
add the following line to the end of the your ~/.bashrc file
```
source ~/OpenFOAM_UMD/OpenFOAM-dev/etc/bashrc
```
then run the following command in the terminal
```
source ~/.bashrc
```


5. Compile the third party library
```
cd ~/OpenFOAM_UMD/ThirdParty-dev
./Allwmake -j >& log.Allwmake &
```
check for errors in the log.Allwmake file


6. Compile the OpenFOAM library
```
cd ~/OpenFOAM_UMD/OpenFOAM-dev
./Allwmake -j >& log.Allwmake &
```
check for errors in the log.Allwmake file





