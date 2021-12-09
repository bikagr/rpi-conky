# rpi-conky

Adding conky to Rapberry Pi4
> sudo apt-get install conky -y


Download the conkyrc file to home directory as .conkyrc
> wget -O /home/pi/.conkyrc https://raw.githubusercontent.com/bikagr/rpi-conky/main/rpi4_conkyrc


Create Shell file
> sudo nano /usr/bin/conky.sh


Add this to shell file to give delay to startup
```
#!/bin/sh
(sleep 10s && conky) &
exit 0
```

Create Conky Autostart file
> sudo nano /etc/xdg/autostart/conky.desktop

Add this to autostart file
```
[Desktop Entry]
Name=conky
Type=Application
Exec=sh /usr/bin/conky.sh
Terminal=false
Comment=system monitoring tool.
Categories=Utility;
```
