# Service-MinecraftServer
Minecraft Server that runs behind a screen session and starts at system startup.

## Install Prerequisites
Installation of Prerequisites

### Java
Java Runtime is needed in order to execute the server command.

#### Ubuntu/Debian
`apt-get install openjdk-17-jre -y`

#### CentOS/AlmaLinux/RockyLinux
`dnf install java-17 -y`

### Screen
Screen is used for being able to interact with the server. It's kind off a second shell which you can connect to.

#### Ubuntu/Debian
`apt-get install screen -y`

#### CentOS/AlmaLinux/RockyLinux
`dnf install screen -y`

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
systemctl daemon-reload
systemctl enable minecraft-serer
systemctl start minecraft-server
screen -r MinecraftServer
```
