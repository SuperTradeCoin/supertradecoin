
Debian
====================
This directory contains files used to package minegoldcoind/minegoldcoin-qt
for Debian-based Linux systems. If you compile minegoldcoind/minegoldcoin-qt yourself, there are some useful files here.

## minegoldcoin: URI support ##


minegoldcoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install minegoldcoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your minegoldcoin-qt binary to `/usr/bin`
and the `../../share/pixmaps/minegoldcoin128.png` to `/usr/share/pixmaps`

minegoldcoin-qt.protocol (KDE)

