# Service-Minecraft-Server
Minecraft Server that runs behind a screen session and starts at system startup.

## Install Prerequisites
Installation of Prerequisites

### Java
Java Runtime is needed in order to execute the server command.

#### Ubuntu/Debian
```
sudo apt-get install openjdk-17-jre -y
```

#### CentOS/AlmaLinux/RockyLinux
```
sudo dnf install java-17 -y
```

### Screen
Screen is used for being able to interact with the server. It's kind off a second shell which you can connect to.

#### Ubuntu/Debian
```
sudo apt-get install screen -y
```

#### CentOS/AlmaLinux/RockyLinux
Epel Release contains the screen package. Install epel-release by `dnf install epel-release -y`
```
sudo dnf install screen -y
```

## Installation
Basically, the installations contains a few steps.
1. Setting up the service file;
2. Preparing the folder for storing all data related to the Minecraft Server;
3. Starting the server.

### Step by Step Installation Commands
The commands below will download the service file, download the jar file, enable the server during system boot, starts the server and connects to the screen session.
```
cd /etc/systemd/system
wget https://raw.githubusercontent.com/mitchellvanbijleveld/Service-MinecraftServer/main/minecraft-server.service
mkdir /etc/minecraft-server
cd /etc/minecraft-server
wget -O minecraft_server.1.19.jar https://launcher.mojang.com/v1/objects/e00c4052dac1d59a1188b2aa9d5a87113aaf1122/server.jar
echo "eula=true" > eula.txt
sudo systemctl daemon-reload
sudo systemctl enable minecraft-server
sudo systemctl start minecraft-server
screen -r MinecraftServer
```

## Interact with the Server
### Starting the server
```
sudo systemctl start minecraft-server
```

### Stopping the server
```
sudo systemctl stop minecraft-server
```

### Connect to Screen session
```
screen -r MinecraftServer
```

To disconnect, pres `Control` + `AD`.

### Enable Server on boot
```
sudo systemctl enable minecraft-server
```

### Disable Server on boot
```
sudo systemctl disable minecraft-server
```

## To Do
- Creating installation script.
