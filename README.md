# RTKBase
From c. 2011 I began creating solutions for survey and hydrography. 
This repo is a rewrite from 2023, with a spec for the simplest RTK Base configuration I can envisage.
It uses str2str from RTKLIB and Linux shell scripts.
It is intended for use with a Raspberry Pi, either at a remote site by a surveyed-in base, or at a fixed, permanent site.

1. Configure the PI and do updates.
2. Enable and test SSH and VNC.
3. Install RTKLIB
```
sudo apt update
sudo apt install git
mkdir rtklib
cd rtklib
git clone https://github.com/rtklibexplorer/RTKLIB.git
```
4. Compile RTKLIB
```
cd RTKLIB/app/consapp/str2str/gcc
make
sudo cp str2str /usr/local/bin/str2str
cd ../../rtkrcv/gcc
make
sudo cp rtkrcv /usr/local/bin/rtkrcv
cd ../../../../..
```
5. Configure the GNSS device.
5. Identify which port you are connecting your GNSS device to.
6. My GNSS is on ttyS0, so my test line is:
```
./str2str -in serial://ttyS0:38400:8:n:1:
```
The output is RTCM3 binary
