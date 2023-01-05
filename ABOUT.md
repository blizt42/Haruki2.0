# Haruki2.0
Music Bot v2.0

Bot created by bamb00#4632 (discord)

Note
----------------------------
* The 4th major version of the discord bot Haruki (V2.0) 
* If you somehow managed to stumble across this page, hi I guess
* With the release of discord py 2.0, slash commands can now be implemented!

> OWO what's this? - Haruki

Requirements
---------------------------
1. install required python modules
  * ffmpeg
  * dnspython
  * googlesearch
  * praw
  * spotipy
  * nekos.py
  * discord.py 2.1.0
  * [libsodium-dev](https://pynacl.readthedocs.io/eb/stable/install/) sudo apt-install libsodium-dev
  * pynacl
  * azurlane
  * youtube_dl
  * pytube
2. raspberry pi stuff
  *(https://www.raspberrypi.org/documentation/linux/usage/systemmd.md/)

Remote ssh (Setup SSH on Pi)
---------------------------
1. `sudo raspi-config`
2. enable ssh
3. [On pc](https://www.raspberrypi.org/documentation/remote-access/ssh/)

Remote file transfer (Setup FTP on Pi)
---------------------------
* https://www.raspberrypi.com/documentation/computers/remote-access.html#sharing-a-folder-from-your-raspberry-pi
1. `sudo apt update`
2. `sudo apt install samba samba-common-bin smbclient cifs-utils`

Install FFMPEG (Setup FFMPEG on Pi)
---------------------------
* https://lindevs.com/install-ffmpeg-on-raspberry-pi/
1. sudo apt update
2. sudo apt install -y ffmpeg

Setup Python with required modules
---------------------------
* https://raspberrytips.com/make-a-discord-bot-on-pi/
* https://stackoverflow.com/questions/63859231/runtimeerror-pynacl-library-needed-in-order-to-use-voice
1. `sudo apt update`
2. `sudo apt upgrade`
3. `sudo apt install python3-pip python3-cffi`
4. `sudo pip3 install -U setuptools`
5. `python3 -m pip install -U discord.py[voice]`

* To test script `python3 HarukiMain.py`
 
Haruki.service (Make HarukiMain.py run as )
---------------------------
* https://jepsonscorner.com/2018/12/20/start-a-python-script-as-a-service-on-your-raspberry-pi/
* https://github.com/blizt42/Haruki.bot/blob/main/ABOUT.md
1. `sudo touch /lib/systemd/system/ServiceScript.service`
2. `sudo nano /lib/systemd/system/ServiceScript.service`

[Unit]
Description=My service
After=network.target

[Service]
ExecStart=/usr/bin/python3 -u HarukiMain.py
WorkingDirectory=/home/pi/Server/HarukiMain/HarukiMain.py
StandardOutput=inherit
StandardError=inherit
Restart=always
User=pi
SyslogIdentifier=HarukiMain

[Install]
WantedBy=multi-user.target

3. `sudo chmod 644 /lib/systemd/system/ServiceScript.service`
4. `sudo systemctl daemon-reload`
5. `sudo systemctl enable ServiceScript.service`

* Enable output into logs
6. `sudo nano /etc/rsyslog.d/ServiceScript.conf`
7. `if $programname==’ServiceScript‘ then /home/pi/Scripts/Logs/ServiceScript.log & stop`
8. `sudo systemctl restart rsyslog`
9. `sudo systemctl start ServiceScript.service`


