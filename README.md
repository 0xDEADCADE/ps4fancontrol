# ps4fancontrol-nogui

Just a simple program to change the fan speed from linux (PS4) (Removed xforms dependency)

## Build

Type 
```
make
```
That's all

## Usage
You need run ps4fancontrol with root privileges
```
sudo ./ps4fancontrol
```
Select your favorite threshold temperature, save and exit.
The selected temperature will be saved in a config file and loaded when ps4fancontrol starts.
If you want load automatically ps4fancontrol at boot of your distro just put
```
ps4fancontrol --no-gui
```
in a unit configuration file: https://wiki.archlinux.org/index.php/Systemd#Writing_unit_files or use crontab or similar..

## Arch Linux users
1) If you are on Arch Linux you can just add the repository https://deadca.de/repo/ps4/os/x86_64 to /etc/pacman.conf
```
sudo echo -e "\n[ps4]\nSigLevel = Optional DatabaseOptional\nServer = https://deadca.de/repo/\$repo/os/\$arch" >> /etc/pacman.conf
```
2) Update Arch Linux
```
sudo pacman -Syu
```
3) Install ps4fancontrol-nogui
```
sudo pacman -S ps4fancontrol-nogui
```
4) Run ps4fancontrol
```
sudo ps4fancontrol
```
5) Select the desidered threshold temperature, save, exit
6) To autostart ps4fancontrol at boot enable the service ps4fancontrol
```
sudo systemctl enable ps4fancontrol
```
Enjoy

## Kudos
Thanks to Zer0xFF for finding the right icc cmd to change the threshold temperature
and to shuffle2 for the patch to expose the icc to usermode.
