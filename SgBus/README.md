Commit your local changes to Git
==================================
1. Using a terminal, go to this project workspace
   > cd /Users/judithpineda/Projects/SgBus/sgbus
2. Commit your local changes to Git using this script:
   > ./git-commit.sh


Deploy SgBus on Raspberry Pi
==================================
1. Login to your Raspberry Pi either via terminal or remote desktop (VNC Viewer).
2. Using a terminal logged in to Raspberry Pi, go to "~/Projects/SgBus"
   > cd ~/Projects/SgBus
3. Clone SgBus project from Github using a script:
   > ./git-clone-sgbus.sh


Auto-start HTTP Server [DONE]
=================================
1. Using a terminal, open "/etc/rc.local"
   > sudo nano /etc/rc.local
2. Add the following commands at the bottom of the script, if they don't exist yet:
   > cd ~/Projects/SgBus/SgBus
   > nohup python -m SimpleHTTPServer &
3. To save and exit, press Ctrl+X, Y, Enter.

Auto-start Chrome browser in Kiosk Mode [DONE]
==============================================
1. Using a terminal, open LXDE config file:
   > sudo nano /home/pi/.config/lxsession/LXDE-pi/autostart
2. Add the following command, if it doesn't exist yet:
   > @chromium-browser --incognito --kiosk http://localhost:8000/index.html
3. To save and exit, press Ctrl+X, Y, Enter.

