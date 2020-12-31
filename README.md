# AMMSfLoL
Mounts Minecraft servers in a ramdisk and restarts them when crashed


The ability to restart on crash minecraft servers is meant to be provided by systemd, you have to use a unit file, there's an example unit file in the repo.


It depends on screen and sudo.



It ensures to run the server as the user that is setup in the configuration, although the script has to be run as root since it needs to handle the ramdisk, when setting up the unit file ensure to leave the user as root and set the minecraft server user in the script instead.

## Usage
AMM_Sf_LoL demonize  # starts the server and periodically saves the server and dumps the ramdisk as well as growing the ramdisk if need be and enough ram



AMM_Sf_LoL start     # starts the server



AMM_Sf_LoL stop      # stops a server that has been run with either start or demonize, it closes the server, dumps the ramdisk and unmounts it



AMM_Sf_LoL help
