# Service-MinecraftServer
Minecraft Server that runs behind a screen session and starts at system startup.

## Prerequisites
- Java JRE 17 is installed
- Screen is installed

## Installation
Basically, the installations contains a few steps.
1. Setting up the service file;
2. Preparing the folder for storing all data related to the Minecraft Server;
3. Starting the server.

### Step by Step Installation Commands
1. `cd /etc/systemd/system`
2. `https://raw.githubusercontent.com/mitchellvanbijleveld/Service-MinecraftServer/main/minecraft-server.service`
3. `mkdir /etc/minecraft-server`
4. `cd /etc/minecraft-server`
5. `wget xxxx`
6. `echo "eula=true" > eula.txt`
7. `systemctl enable minecraft-serer`
8. `systemctl start minecraft-server`
9. `screen -r MinecraftServer`
