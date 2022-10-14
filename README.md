# Centos-7
This contains steps to convert Centos Minimal to GUI
**I am trying to make this as simple as possible. The first thing you have to make sure is don't skip any part and read everything before you enter any command. **
lets get started
First step is login through root user
_ (Make sure you are connected to internet) _
the next step is to install "epel"
yum install epel-release.noarch
yum update epel-release.noarch yum install bash* yum install wget yum install vim
_if you prefer nano editor _
yum install nano  yum install net-tools
Check the groups select if you want GNOME or any other
yum group list 
_ I am selecting MATE Desktop _
yum groupsinstall "MATE Desktop" yum groupsinstall "Server with GUI"
_typing the next command will start the GUI mode _
startx
To set GUI to default following command
systemctl get-default systemctl set-default graphical.target systemctl isolate graphical.target
_now restart and it will load in GUI _
init 6
