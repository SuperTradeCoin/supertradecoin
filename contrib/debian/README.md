
Debian
====================
This directory contains files used to package supertradecoind/supertradecoin-qt
for Debian-based Linux systems. If you compile supertradecoind/supertradecoin-qt yourself, there are some useful files here.

## supertradecoin: URI support ##


supertradecoin-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install supertradecoin-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your supertradecoin-qt binary to `/usr/bin`
and the `../../share/pixmaps/supertradecoin128.png` to `/usr/share/pixmaps`

supertradecoin-qt.protocol (KDE)

