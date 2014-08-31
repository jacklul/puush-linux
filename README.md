puush-linux
===========
Bash script to provide puush.me screenshot and file upload functionality for linux users.

_Rewrite of script created by Sunmock Yang (https://github.com/sunmockyang/puush-linux)_

## Dependencies
 - scrot
 - curl
 - xclip
 - notify-send (notify-osd package)
 - zenity (optional for file selector, without it -f option will be unavailable)

## Installation
- Clone/[Download](https://github.com/jacklul/puush-linux/archive/master.zip) this repository, unzip it then navigate to **puush-linux-master** directory
- Run **puush-install** as root.
- Done, you can remove unpacked files.

First time you will run **puush** command it will ask you for API key, see [puush.me Account Settings](http://puush.me/account/settings) to get yours, if you started the command from outside the terminal (keyboard shortcut) you will have to enter your API key manually in *~/.config/puush/puush.conf* file.

## Usage
Set up keyboard shortcuts within linux (in Ubuntu it's *System Settings > Keyboard > Keyboard Shortcuts > Custom Shortcuts*)

| command  | description |
| ------------- | ------------- |
| puush -d  | puush desktop  |
| puush -w  | puush window  |
| puush -a  | puush area  |
| puush -f  | upload file  |

### Nautilus integration
Sample Nautilus script:
```
#!/bin/bash

for arg 
do
	puush "$arg"
done
```
