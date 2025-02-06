# Xemu Setup for Retropie

This will add an entry on [Retropie-Setup](https://github.com/RetroPie/RetroPie-Setup) for [Xemu Emulator](https://github.com/xemu-project/xemu) running on a ARM64 (aka Raspberry) machine.

## Requirements

Check if you have Xbox already listed in file `~/RetroPie-Setup/platforms.cfg`.

If not, create (or edit) file `/opt/retropie/configs/all/platforms.cfg` and add:

```
switch_exts=".iso"
switch_fullname="xbox"
```

## Install

After that, install the Lime3ds setup script with:

```bash
sudo apt install -y flatpak
sudo flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub app.xemu.xemu
```

Now you can run **RetroPie Setup** script and `xemu` will available under `exp` (experimental) packages section.
