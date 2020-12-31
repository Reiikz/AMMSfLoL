# AMMSfLoL
Mounts Minecraft servers in a ramdisk and restarts them when crashed

The ability to restart minecraft servers on crash you have to use a unit file, there's an example unit file in the repo.


It depends on screen and sudo.
It ensures to run the server as the user that is setup in the configuration, although the script has to be run as root since it needs to handle the ramdisk, when setting up the unit file ensure to leave the user as root and set the minecraft server user in the script instead.
