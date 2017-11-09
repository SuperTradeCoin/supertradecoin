MineGoldCoin 1.8.1
====================

* Copyright (c) 2009-2014 Bitcoin Developers
* Copyright (c) 2011-2013 Litecoin Developers
* Copyright (c) 2013-2014 MineGoldCoin Developers


Setup
---------------------
[MineGoldCoin Core](http://minegoldcoin.com/en/download) is the original MineGoldCoin client and it builds the backbone of the network. However, it downloads and stores the entire history of MineGoldCoin transactions (which is currently several GBs); depending on the speed of your computer and network connection, the synchronization process can take anywhere from a few hours to a day or more. Thankfully you only have to do this once. If you would like the process to go faster you can [download the blockchain directly](bootstrap.md)

Running
---------------------
The following are some helpful notes on how to run MineGoldCoin on your native platform. 

### Unix

You need the Qt4 run-time libraries to run MineGoldCoin-Qt. On Debian or Ubuntu:

	sudo apt-get install libqtgui4

Unpack the files into a directory and run:

- bin/32/minegoldcoin-qt (GUI, 32-bit) or bin/32/minegoldcoind (headless, 32-bit)
- bin/64/minegoldcoin-qt (GUI, 64-bit) or bin/64/minegoldcoind (headless, 64-bit)



### Windows

Unpack the files into a directory, and then run minegoldcoin-qt.exe.

### OSX

Drag MineGoldCoin-Qt to your applications folder, and then run MineGoldCoin-Qt.

### Need Help?

* See the documentation at the [MineGoldCoin Wiki](http://dogeco.in/)
for help and more information.
* Ask for help on [#minegoldcoin](http://webchat.freenode.net?channels=minegoldcoin) on Freenode. If you don't have an IRC client use [webchat here](http://webchat.freenode.net?channels=minegoldcoin).
* Ask for help on the [/r/dogeducation subreddit](http://reddit.com/r/dogeducation).

Building
---------------------
The following are developer notes on how to build MineGoldCoin on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

- [OSX Build Notes](build-osx.md)
- [Unix Build Notes](build-unix.md)
- [Windows Build Notes](build-msw.md)

Development
---------------------
The MineGoldCoin repo's [root README](https://github.com/minegoldcoin/minegoldcoin/blob/master/README.md) contains relevant information on the development process and automated testing.

- [Coding Guidelines](coding.md)
- [Multiwallet Qt Development](multiwallet-qt.md)
- [Release Notes](release-notes.md)
- [Release Process](release-process.md)
- [Source Code Documentation (External Link)](https://dev.visucore.com/bitcoin/doxygen/)
- [Translation Process](translation_process.md)
- [Unit Tests](unit-tests.md)

### Resources
* Discuss on the [/r/minegoldcoindev](http://www.reddit.com/r/minegoldcoindev) subreddit.
* Discuss on [#minegoldcoin-dev](http://webchat.freenode.net/?channels=minegoldcoin-dev) on Freenode. If you don't have an IRC client use [webchat here](http://webchat.freenode.net/?channels=minegoldcoin-dev).

### Miscellaneous
- [Assets Attribution](assets-attribution.md)
- [Files](files.md)
- [Tor Support](tor.md)

License
---------------------
Distributed under the [MIT/X11 software license](http://www.opensource.org/licenses/mit-license.php).
This product includes software developed by the OpenSSL Project for use in the [OpenSSL Toolkit](http://www.openssl.org/). This product includes
cryptographic software written by Eric Young ([eay@cryptsoft.com](mailto:eay@cryptsoft.com)), and UPnP software written by Thomas Bernard.
