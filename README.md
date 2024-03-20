**Hyprland SETUP for AlpineLinux**

![image](https://github.com/ronardnx/hyprland_alpinelinux/assets/23416091/ef390290-3635-47f8-a225-cc54e17d59ec)


_Basic Requirements:_

  -  a device with alpine linux (duh),
  -  hyprland, waybar, rofi-wayland, nwg-look(@nwg-piotr/nwg-look),kitty and kitty-kitten for the basic interaction with my dots
  -   your GPU Mesa driver (mesa-egl for amdgpu and mesa-dri-gallium for amd)
  -   brightnessctl, pulseaudio, mako(notify daemon), grim, wl-clipboard, slurp (screenshots), librsvg, swaybg (background img daemon), mate-polkit (necessary), fish shell, seatd ( wiithout it Hyprland will not work), consolekit2, starship,lf  and maybe more ( you can check my hyprland config)

_Setup:_

**1.** Install the provided packages.

**2.** Copy my dots over your.config and .local. 

git clone https://github.com/ronardnx/hyprland_alpinelinux &&
cd hyprland_alpinelinux &&
rm -rf .git && 
cp -r .local/* ~/.local/ &&
cp -r .config/* 

**3.** Setup your daemons and groups:

doas setup-devd udev &&
doas rc-update add elogind &&
doas rc-update add polkit &&
chsh -s /usr/bin/fish &&
doas useradd $USER seat &&
doas useradd $USER video && 
doas reboot

**4.** Starting the setup.

Login from tty and type startx (that s my alias for dbus-run-session Hyprland)

_Cheatsheet:_

**mod + D**  - launches rofi ,
**mod + SHIFT + SPACE** change the layout from tilling to floating,
**mod + SHIFT + Return** launches kitty,
**your stock acpi**(Fn + ...) keys for PRINT, volume and brightness will work just good.

_for more just read my config file_
