Reicast emulator precompiled for fixing exit cleanly and save NVRAM

It's a drop-in replacement for the file in /opt/retropie/emulators/reicast/bin. It contains @Toxicshadow's Linux fixes so Reicast can exit cleanly and save NVRAM settings.



To use it, download the "reicast" file, copy it to /home/pi and run these commands:

cd /opt/retropie/emulators/reicast/bin

sudo mv reicast reicast_old

sudo cp /home/pi/reicast reicast

sudo chmod 755 reicast



This will go into the directory and rename the previous "reicast" file to "reicast_old", then copy the new file in, and then change the new file's mode to be executable.


If you want to put the old one back (if for some reason the new one doesn't work right), run these commands from the shell, which will delete the new file and replace it with the old one:

cd /opt/retropie/emulators/reicast/bin

sudo rm reicast

sudo mv reicast_old reicast
