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
```
cd /etc/systemd/system
wget https://raw.githubusercontent.com/mitchellvanbijleveld/Service-MinecraftServer/main/minecraft-server.service
mkdir /etc/minecraft-server
cd /etc/minecraft-server
wget -O minecraft_server.1.19.jar https://launcher.mojang.com/v1/objects/e00c4052dac1d59a1188b2aa9d5a87113aaf1122/server.jar
echo "eula=true" > eula.txt
systemctl enable minecraft-serer
systemctl start minecraft-server
screen -r MinecraftServer
```
