# **Welcome to Raspberry Pi Sluggish Video Fixer Manual**
I have raspberry pi 4 B with **Raspbian OS**. Connected it to 55" TV via HDMI cable and connected it to WiFi. I opened chromium and went to watch yourube video. Everything runs perfectly until I go to full screen. Then it started running sluggish. Frames dropted, video and sound went unsynced and it was for every page I opened on web browser. I searched everywhere, tried multiple web browsers, enabled hardware acceleration.... Nothing worked. I tougth maybe it is pi problem. So I downloaded short video in 4k and launched it wiht VLC media player. The image and sound were perfect in full screen. That means it is browser problem. I tried sending data strait to vlc player from chromium and firefox but couldn't do it. The add-ons require some client-software installed but not for *arm architecture*. Now about the fix. For this one desktop is required!
# **1. - Install stremio**
[**Shivasiddharth**](https://github.com/shivasiddharth) managed to compile stremio for arm architecture. If you want you can follow his [**walktrough**](https://github.com/shivasiddharth/Stremio-RaspberryPi/blob/master/README.md) or stick here and later please go there to buy him a coffe, provide feedback and give a star or positive review. First we need to download zip file that contains binaries. Download it from his site [**here**](https://github.com/shivasiddharth/Stremio-RaspberryPi/releases/tag/4.4.142). Move it from ```Downloads``` folder to ```~``` folder
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
Change ```stremio_x.x.xxx-1_arm``` to your version. Now you should have it installed. Open it.
# **2. - Configure stremio**
Click on top right puzzle icon

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/e9c9fdc5-40e2-4897-a294-54e6186abfc8)

Now add the ones you want. Go back to home page and choose the movie or series you like

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/7b41eb2f-9735-4947-b223-02087d37445f)

Click to watch it

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/00a0aa4f-caaf-471d-a8fc-b8c3d157bf94)

**When it starts, pauze it!**

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/98d0cf7f-6d5f-4bf8-a5b1-09a9e087fa85)

Now click on settings button and choose ```Watch on VLC```

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/612404af-d6cb-4297-8faf-6047d4f610c6)

The movie will be opened in VLC Media player and it should not be sluggish. Remember not to run it like me in RealVNC, but dirrectly on monitor! 

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/c06e6ab8-9ede-4f73-9166-a5f147ecc94b)

# **3. - Add subtitles**
You can add subtitles by clicking on View -> VLsub

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/ddc64263-6bf5-4adf-a634-e67b0c865c47)

Click ```Search by hash```

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/01c4eff1-f41d-4344-adc8-5cc2b309fc63)

Click on the result

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/e0b34c34-3554-4ebb-8ee3-49023d883ff2)

Download the selection

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/10f8d7ca-26c7-40c3-86ac-2b56909b7e6a)

Close and enjoy your movie! If you can't hear anything, right-click on top right of you desktop bar and choose ```HDMI``` as your output

![image](https://github.com/GoranSustekJr/Raspberry-Pi-Sluggish-Video-Fixer/assets/139004385/1da5a223-03c4-4dbb-a684-7db1edd3b707)

If you want, play with VLC media player to optimize sound, picture and subtitles. If it is still slugish, it is probably internet connection. If you can't hear anything, right-click on top right of you desktop bar and choose ```HDMI``` as your output and enjoy your movie in **full screen**! 
