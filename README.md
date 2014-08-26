puush-linux
===========
Bash script to provide puush.me screenshot and file upload functionality for linux users.

_Rewrite of script created by Sunmock Yang (https://github.com/sunmockyang/puush-linux)_

## Dependencies
 - gnome-screenshot
 - curl
 - xclip
 - notify-send (notify-osd)

_This script was essentially written for Ubuntu and Gnome, I have no idea how it will work on other distros/desktop environments._

## Installation
- Clone/[download](https://github.com/jacklul/puush-linux/archive/master.zip) this repository, unzip it then navigate to **puush-linux-master** directory
- Run **puush-install** as root.
- Done, you can remove unpacked files.

First time you will run **puush** command it will ask you for API key, see [puush.me Account Settings](http://puush.me/account/settings) to get yours.

## Usage
Set up keyboard shortcuts within linux (in Ubuntu it's *System Settings > Keyboard > Keyboard Shortcuts > Custom Shortcuts*)

| command  | description | (recommended keyboard shortcut) |
| ------------- | ------------- | ------------- |
| puush -d  | puush desktop  | (Ctrl + Shift + 3/#)  |
| puush -w  | puush window  | (Ctrl + Shift + 2/@)  |
| puush -a  | puush area  | (Ctrl + Shift + 4/$)  |
| puush -f  | upload file  | (Ctrl + Shift + U)  |

You can also use these commands in terminal.

### Nautilus integration
Sample Nautilus script:
```
#!/bin/bash

for arg 
do
	puush "$arg"
done
```
