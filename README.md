# Centos-7

## Minimal to GUI

***This contains steps to convert Centos 7 Minimal to GUI***

***I am trying to make this as simple as possible. The first thing you have to make sure is don't skip any part and read everything before you enter any command.***

***Lets get started***

***First step is login through root user
(Make sure you are connected to internet)***

***The next step is to install "epel"***
```
yum install epel-release.noarch
```
```
yum update epel-release.noarch 
```
```
yum install bash* 
```
```
yum install wget
```
```
yum install vim
```
***if you prefer nano editor***

```
yum install nano
```

```
yum install net-tools
```
***Check the groups select if you want GNOME or any other***
```
yum group list 
```
***I am selecting MATE Desktop***
```
yum groupsinstall "MATE Desktop"
```
```
yum groupsinstall "Server with GUI"
```
***Typing the next command will start the GUI mode***
```
startx
```
***To set GUI to default following command***
```
systemctl get-default
```
```
systemctl set-default graphical.target
```
```
systemctl isolate graphical.target
```
***Now restart and it will load in GUI***
```
init 6
```
