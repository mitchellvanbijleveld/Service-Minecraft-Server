# Service-MinecraftServer
Minecraft Server that runs behind a screen session and starts at system startup.

## Prerequisites
- Java openJDK 17 is installed
- Screen is installed

## Installation
1. Create directory /etc/minecraft-server
2. `cd` into /etc/minecraft-server
3. download latest minecraft server jar
4. `systemctl enable minecraft-server`
5. `systemctl start minecraft-server`

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
