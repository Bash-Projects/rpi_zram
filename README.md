# rpi_zram
Script to dynamically enable ZRAM on a Raspberry Pi or other Linux system.

Automatically detects the number of CPU cores to allocate to ZRAM computation, disables existing swap and enables ZRAM swap.

## Mi método

> sudo wget -O /usr/bin/zram.sh https://raw.githubusercontent.com/Bash-Projects/rpi_zram/master/zram.sh

> sudo chmod +x /usr/bin/zram.sh

> echo -e "#!/bin/bash \n /usr/bin/zram.sh &" >  /home/marc/scripts/zram.sh

Sustituye usuario por tu usuario
> @reboot ( sleep 50 ; sudo /home/usuario/scripts/zram.sh )

> sudo reboot now

## Original

Download the script and copy to /usr/bin/ folder
> sudo wget -O /usr/bin/zram.sh https://raw.githubusercontent.com/novaspirit/rpi_zram/master/zram.sh

make file executable
> sudo chmod +x /usr/bin/zram.sh

edit /etc/rc.local file to run script on boot
> sudo nano /etc/rc.local

add line before exit 0
> /usr/bin/zram.sh &
