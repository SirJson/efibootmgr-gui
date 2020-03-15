# efibootmgr-gui+

Manage EFI boot loader entries or directly reboot to the selected target with this simple GUI.
This fork adds two buttons, one for reboot and one for shutdown for easier dual booting.

Eventually I might strip the other functionality to make it more like a shutdown / reboot / logout helper with OS selection.

## Dependencies

If you are using Debian GNU/Linux:

```
sudo apt install efibootmgr python3
```

Not all distros install **pyhton-gobject** automatically with Python3, but it is required to run this script.

For Arch users:

```
sudo pacman -S efibootmgr python3 python-gobject
```

My modification assumes you are on a distro with systemd.

To make the shutdown or reboot button work your user needs permission to do so. I tested this on Ubuntu 19.10 and didn't need any modifications but your mileage may vary.

## Usage

```
python3 efibootmgr_gui.py
# that should be the same as
./efibootmgr_gui.py
```

**Note**: This program assumes that the EFI System Partition (ESP) is mounted at
`/boot/efi`.
However you can use --efi=/dev/sd?? (e.g. sda1) to manually specify your
EFI System Partition (ESP).
