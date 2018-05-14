SuperTradeCoin 1.8.1
====================

* Copyright (c) 2009-2014 Bitcoin Developers
* Copyright (c) 2011-2013 Litecoin Developers
* Copyright (c) 2013-2014 SuperTradeCoin Developers


Setup
---------------------
[SuperTradeCoin Core](http://supertradecoin.com/en/download) is the original SuperTradeCoin client and it builds the backbone of the network. However, it downloads and stores the entire history of SuperTradeCoin transactions (which is currently several GBs); depending on the speed of your computer and network connection, the synchronization process can take anywhere from a few hours to a day or more. Thankfully you only have to do this once. If you would like the process to go faster you can [download the blockchain directly](bootstrap.md)

Running
---------------------
The following are some helpful notes on how to run SuperTradeCoin on your native platform. 

### Unix

You need the Qt4 run-time libraries to run SuperTradeCoin-Qt. On Debian or Ubuntu:

	sudo apt-get install libqtgui4

Unpack the files into a directory and run:

- bin/32/supertradecoin-qt (GUI, 32-bit) or bin/32/supertradecoind (headless, 32-bit)
- bin/64/supertradecoin-qt (GUI, 64-bit) or bin/64/supertradecoind (headless, 64-bit)



### Windows

Unpack the files into a directory, and then run supertradecoin-qt.exe.

### OSX

Drag SuperTradeCoin-Qt to your applications folder, and then run SuperTradeCoin-Qt.

### Need Help?

* See the documentation at the [SuperTradeCoin Wiki](http://dogeco.in/)
for help and more information.
* Ask for help on [#supertradecoin](http://webchat.freenode.net?channels=supertradecoin) on Freenode. If you don't have an IRC client use [webchat here](http://webchat.freenode.net?channels=supertradecoin).
* Ask for help on the [/r/dogeducation subreddit](http://reddit.com/r/dogeducation).

Building
---------------------
The following are developer notes on how to build SuperTradeCoin on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

- [OSX Build Notes](build-osx.md)
- [Unix Build Notes](build-unix.md)
- [Windows Build Notes](build-msw.md)

Development
---------------------
The SuperTradeCoin repo's [root README](https://github.com/supertradecoin/supertradecoin/blob/master/README.md) contains relevant information on the development process and automated testing.

- [Coding Guidelines](coding.md)
- [Multiwallet Qt Development](multiwallet-qt.md)
- [Release Notes](release-notes.md)
- [Release Process](release-process.md)
- [Source Code Documentation (External Link)](https://dev.visucore.com/bitcoin/doxygen/)
- [Translation Process](translation_process.md)
- [Unit Tests](unit-tests.md)

### Resources
* Discuss on the [/r/supertradecoindev](http://www.reddit.com/r/supertradecoindev) subreddit.
* Discuss on [#supertradecoin-dev](http://webchat.freenode.net/?channels=supertradecoin-dev) on Freenode. If you don't have an IRC client use [webchat here](http://webchat.freenode.net/?channels=supertradecoin-dev).

### Miscellaneous
- [Assets Attribution](assets-attribution.md)
- [Files](files.md)
- [Tor Support](tor.md)

License
---------------------
Distributed under the [MIT/X11 software license](http://www.opensource.org/licenses/mit-license.php).
This product includes software developed by the OpenSSL Project for use in the [OpenSSL Toolkit](http://www.openssl.org/). This product includes
cryptographic software written by Eric Young ([eay@cryptsoft.com](mailto:eay@cryptsoft.com)), and UPnP software written by Thomas Bernard.
