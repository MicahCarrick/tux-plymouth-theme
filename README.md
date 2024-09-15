# Linux "Tux" Penguin Boot Splash Screen

![example splash](example2.png)

A [Plymouth](https://www.freedesktop.org/wiki/Software/Plymouth/) boot splash screen depicting the ["Tux"](https://en.wikipedia.org/wiki/Tux_(mascot)) mascot.

This is a fork of [tux-plymouth-theme](https://github.com/Tux4Ubuntu/tux-plymouth-theme) by *tux4ubuntu* with some changes to suite my personal preferences:


* Removed shutdown images--shows the same simple "Tux" image on boot and on shutdown
* Removed progress bar
* Extended the width of encryption password input field
* Does not render bullets in the password input if the characters exceed with width ofthe input box

## Installation

These instructions have been verified on Fedora 40 See also See: [plymouth-set-default-theme](https://man.archlinux.org/man/plymouth-set-default-theme.1.en) man page.

Copy src to Plymouth theme folder:

```shell
sudo mkdir /usr/share/plymouth/themes/tux-plymouth-theme
sudo cp -r src/* /usr/share/plymouth/themes/tux-plymouth-theme
```

Set `tux-plymouth-theme` as the default Plymouth theme and rebuild the image:

```shell
sudo plymouth-set-default-theme -R tux-plymouth-theme
```
