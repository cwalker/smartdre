# smartdre

Developing / Testing Version

A script to download a docker image, install dependencies and run the drivers/software 
for old digital boards "SmartBoard" in new ubuntu based distros.

Docker image based on Ubuntu 12.04 "Precise"

Gracias al equipo de Lliurex Team, basé mi dockerfile en el suyo y usé sus archivos .deb.

Thanks Lliurex Team
lliurex.net

## USAGE

    cd ~ 

    git clone https://github.com/aosucas499/smartdre.git

    cd smartdre

    ./install-smartdre


## FILES description

### install-smartdre: Run first. It installs: 
1. Docker. 
2. Driver dependencies needed for the digital board in the host system. ("nwferi-daemon", "nwfermi-module" and "xf86-input-nextwindow")
   Thanks to https://github.com/glorang, Daniel Newton and Lliurex TEAM.
3. Docker image (aosucas499/smartdre)
4. File to boot at init session (it copies the file smartdre.desktop to ~/.config/autostart)

### smartdre.desktop
File necessary to boot the container when the session starts. It will be copied to folder "~/.config/autostart", compatible with KDE and GNOME.

### smartdre
It runs the the docker container, taking into account if the container was created or not.

>## IMPORTANT
 Don't move this script from the folder "~/smartdre/" or it won't work
 because the autoboot file finds the script in that folder

>## IMPORTANTE
 No muevas este script de la carpeta "~/smartdre" o no funcionará
 porque el archivo de autoarranque busca este script en esa carpeta
