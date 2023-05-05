## Keymap
Allows use outside of xserver

Store file in ```/usr/share/kbd/keymaps/i386/dvorak/```
```
sudo cp dvorak-real-programmer.map /usr/share/kbd/keymaps/i386/dvorak/
```
If stored outside of ```/usr/share/kbd/keymaps/``` full path must be specified in the commands below

set keymap for current session:
```
sudo loadkeys dvorak-real-programmer
```

## Persistent configuration
*localectl* changes the ```KEYMAP``` variable in ```/etc/vconsole.conf``` and sets the keymap for the current session
```
sudo localectl set-keymap dvorak-real-programmer
```

alternatively manually edit ```/etc/vconsole.conf``` to say:
```
KEYMAP=dvorak-real-programmer
```

more: https://wiki.archlinux.org/title/Linux_console/Keyboard_configuration
