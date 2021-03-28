# Useful Linux Stuff (focus on Artix)


## !! Drivers !!
* If installed linux-lts, install nvidia lts drivers
* Apparently it might sometimes help to have an empty `etc/X11/xorg.conf` file. And it rather *has* to be empty

## Xrandr
* [Mixed monitors xrandr](https://blog.summercat.com/configuring-mixed-dpi-monitors-with-xrandr.html)
* Gui control for `xrandr`: `arandr`

## Correct time (with summer time change)
* Install `ntp` and `ntp-openrc`. Easily configured with `timeset-gui` (AUR)

## Discord emojis (twemoji) on the system and dmenu:
* [System installation](https://partage.les-miquelots.net/engver/blog/how-to-have-colored-emojis-in-dmenu-st-dwm-and-slstatus-on-archlinux.html)
* Dmenu and other suckless: fonts must resemble this: `static const char *fonts[] = {
	"monospace:size=10", "twemoji"
};`
* There is a part of dmenu's code that has to be removed, the comment specifies it blocks colored glyphs

## Virtualbox:
* Currently official stuff is broken, the script from the official page works

## Bluetooth devices:
* With pulse, proceed as indicated in the [wiki](https://wiki.archlinux.org/index.php/Bluetooth#PulseAudio), that means install `pulseaudio-bluetooth` and add `load-module module-bluetooth-policy
load-module module-bluetooth-discover` at the end of `/etc/pulse/system.pa` and reboot

## Wiimotes/Dolphin:
* If connecting as xbox360 gamepad: Connect using `blueman`. Add wiimote using moltengamepad, use the flag setting it up as an xbox360 device, because otherwise linux sees a wiimote, it's ir and the nunchuk as separate devices (rumble optional): `sudo moltengamepad --mimic-xpad --rumble`
* If using dolphin: do not use `blueman`, it can actually interfere. Just press buttons 1 and 2 while `dolphin` runs. Be sure to select real wiimotes in settings. Connecting wiimotes when a game is already running will not add them to the game.
* Use [NUS Downloader](https://wiibrew.org/wiki/NUS_Downloader) in virtualbox or Windows machine to get the mii channel and launch the wda file like a game, not via the wii system menu.

## Linux alternatives by Dbp:
### GUI:
* Calculator > qalculate(-gtk)
* Explorer/Winfile > XFE/Thunar
* Internet Explorer/Edge > Surf/LibreWolf/Degoogled Chromium
* Outlook > Thunderbird
* Paint/.net > Pinta
* VSXX > VSC?
* WordPad > Abiword
* Notepad/++ > leafpad(use tabbed for tabs)
* Windows Media Player/MPC > VLC
* Windows Photo Viewer > GPicview/Viewnior
* MS Office > LibreOffice
* Cmd > Urxvt
* Powertoys > DWM
* Task Manager > LXTask
* WinSCP > filezilla / muCommander
* Logitech gaming software > piper

### CLI:
* Internet Explorer > Lynx
* Outlook > Mutt
* Notepad/++ > Micro/Vis
* Windows Media Player/MPC > MPV/MOC
* Windows Photo Viewer > viu
* Task Manager > htop

## Ricing Guides:
* [dwm status](https://www.youtube.com/watch?v=6vTrVPpNodI&t=1515)
* [urxvt](https://www.youtube.com/watch?v=OVko_lhkQjs)

## Extra Resources
* [Synopta](https://addons.mozilla.org/en-US/firefox/addon/add-custom-search-engine/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search)
* [https://wiki.installgentoo.com/wiki/List_of_recommended_GNU/Linux_software](https://wiki.installgentoo.com/wiki/List_of_recommended_GNU/Linux_software)
* [https://suckless.org/sucks/](https://suckless.org/sucks/)
* [https://suckless.org/rocks/](https://suckless.org/rocks/)
* [https://privacytools.io/](https://privacytools.io/)
* [https://www.fsf.org/resources/](https://www.fsf.org/resources/)
* [https://www.gnu.org/software/software.html](https://www.gnu.org/software/software.html)
* [https://github.com/mayfrost/guides/blob/master/ALTERNATIVES.md](https://github.com/mayfrost/guides/blob/master/ALTERNATIVES.md )

## Misc
* [urxvt](https://github.com/charnley/dotfiles.x/blob/master/Xresources)
* [Smoking Spectre dotfiles](https://github.com/SmokinSpectre/Dots)
* [wolfiy](https://gitlab.com/wolfiy)
* [Bot converting telegram sticker packs to signal](https://t.me/telesignal_bot)

## Notes/TODO:
* Rice dwm and dstatus, ~~patch dwm so the status is on all screens~~
* setup and rice [these](https://github.com/dudik/herbe) toasts. They can be killed with a precise `kill` command, bind it to dwm and voilà
* daemonize isync