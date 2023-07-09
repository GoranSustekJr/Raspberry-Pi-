# **Welcome to Raspberry Pi Sluggish Video Fixer Manual**
I have raspberry pi 4 B with **Raspbian OS**. Connected it to 55" TV via HDMI cable and connected it to WiFi. I opened chromium and went to watch yourube video. Everything runs perfectly until I go to full screen. Then it started running sluggish. Frames dropted, video and sound went unsynced and it was for every page I opened on web browser. I searched everywhere, tried multiple web browsers, enabled hardware acceleration.... Nothing worked. I tougth maybe it is pi problem. So I downloaded short video in 4k and launched it wiht VLC media player. The image and sound were perfect in full screen. That means it is browser problem. I tried sending data strait to vlc player from chromium and firefox but couldn't do it. The add-ons require some client-software installed but not for *arm architecture*. Now about the fix. For this one desktop is required!
# **1. - Install stremio**
[**Shivasiddharth**](https://github.com/shivasiddharth) managed to compile stremio for arm architecture. If you want you can follow his [**walktrough**](https://github.com/shivasiddharth/Stremio-RaspberryPi/blob/master/README.md) or stick here and after go there and start, provide feedback and give a star or positive review. First we need to download zip file that contains binaries. Download it from his site [**here**](https://github.com/shivasiddharth/Stremio-RaspberryPi/releases/tag/4.4.142). Move it from ```Downloads``` folder to ```~``` folder
```
mv ${File path} ~
```
Make sure to change ```${File path}``` to your file path of the zip file. Now unzip it
```
unzip ${file}
```
**Change file to the file you downloaded. Run the following commands**
- For Buster users:
```
sudo sh -c "echo 'deb http://ftp.us.debian.org/debian/ buster main contrib non-free' >> /etc/apt/sources.list"   
sudo sh -c "echo 'deb http://deb.debian.org/debian buster main contrib non-free' >> /etc/apt/sources.list"     
sudo apt-get update 
```
- For Bullseye users:
```
sudo sh -c "echo 'deb http://ftp.us.debian.org/debian/ bullseye main contrib non-free' >> /etc/apt/sources.list"    
sudo sh -c "echo 'deb http://deb.debian.org/debian bullseye main contrib non-free' >> /etc/apt/sources.list"    
sudo apt-get update
```
**Change the directory:**
- For 64-bit users:
```
cd /home/${USER}/Stremio-x.x.xxx-arm64-64-bit/
```
- For 32-bit users:
```
cd /home/${USER}/Stremio-x.x.xxx-armhf-32-bit/
```
Remember to change ```Stremio-x.x.xxx-arm...``` to your version
**Preform the installation:**
- For 64-bit users:
```
sudo apt-get install ./libfdk-aac1_0.1.6-1_arm64.deb ./stremio_x.x.xxx-1_arm64.deb -f
```
- For 32-bit users:
```
sudo apt-get install ./libfdk-aac1_0.1.6-1_armhf.deb ./stremio_x.x.xxx-1_armhf.deb -f   
```
Change ```stremio_x.x.xxx-1_arm``` to your version. Now you should have it installed. Next add some add-ons.
