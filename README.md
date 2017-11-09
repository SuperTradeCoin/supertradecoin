# MineGoldCoin Core [MGC]
==========================

![MineGoldCoin](http://static.tumblr.com/ppdj5y9/Ae9mxmxtp/300coin.png)

[![Build Status](https://travis-ci.org/minegoldcoin/minegoldcoin.svg?branch=1.7-dev)](https://travis-ci.org/minegoldcoin/minegoldcoin) [![tip for next commit](https://tip4commit.com/projects/702.svg)](https://tip4commit.com/github/minegoldcoin/minegoldcoin)

## What is MineGoldCoin? – Such coin
MineGoldCoin is a cryptocurrency like Bitcoin, although it does not use SHA256 as its proof of work (POW). Taking development cues from Tenebrix and Litecoin, MineGoldCoin currently employs a simplified variant of scrypt.

http://minegoldcoin.com/

## License – Much license
MineGoldCoin is released under the terms of the MIT license. See [COPYING](COPYING)
for more information or see http://opensource.org/licenses/MIT.

## Development and contributions – omg developers
Development is ongoing and the development team as well as other volunteers can freely work in their own trees and submit pull requests when features or bug fixes are ready.

#### Version strategy
Version numbers are following ```major.minor.patch``` semantics.

#### Branches
There are 3 types of branches in this repository:

- **master:** Stable, contains the latest version of the latest *major.minor* release.
- **maintenance:** Stable, contains the latest version of previous releases, which are still under active maintenance. Format: ```<version>-maint```
- **development:** Unstable, contains new code for planned releases. Format: ```<version>-dev```

*Master and maintenance branches are exclusively mutable by release. Planned releases will always have a development branch and pull requests should be submitted against those. Maintenance branches are there for* ***bug fixes only,*** *please submit new features against the development branch with the highest version.*

## Very Much Frequently Asked Questions

### How much doge can exist? – So many puppies!
Early 2017 (approximately a year and a half after release) there will be approximately 100,000,000,000 coins.
Each subsequent block will grant 10,000 coins to encourage miners to continue to secure the network and make up for lost wallets on hard drives/phones/lost encryption passwords/etc.

### How to get doge? – To the moon!
MineGoldCoin uses a simplified variant of the scrypt key derivation function as its proof of work with a target time of one minute per block and difficulty readjustment after every block. The block rewards are fixed and halve every 100,000 blocks. Starting with the 600,000th block, a permanent reward of 10,000 MineGoldCoin per block will be paid. 

Originally, a different payout scheme was envisioned with block rewards being determined by taking the maximum reward as per the block schedule and applying the result of a Mersenne Twister pseudo-random number generator to arrive at a number between 0 and the maximum reward. This was changed, starting with block 145,000, to prevent large pools from gaming the system and mining only high reward blocks. At the same time, the difficulty retargeting was also changed from four hours to once per block (every minute), implementing an algorithm courtesy of the DigiByte Coin development team, to lessen the impact of sudden increases and decreases of network hashing rate.

Currency unit : MGC
Algorithm : Scrypt
Block Interval : 1 minute (60 seconds)
Difficulty Retarget : Every block (using Kimoto's Gravity Well)
Total coins amount : 25,000,000 MGC
Block reward 
Premine: First 10 block are 2,500,000 HVC 
Bonus reward for block 10,000 to 100,000 of 3.5 coins
Bonus reward for block 400,000 - 800,000 of 5 coins
Bonus reward for block 400,000 - 1,200,000 of 15 coins
Bonus reward for block 1,200,000 - 1,600,000 of 20 coins
Subsidy is cut in half every 400,000 blocks starting at block 1600000
Premine : None
 
  
### Overview plz make minegoldcoind/minegoldcoin-cli/minegoldcoin-qt

  The following are developer notes on how to build MineGoldCoin on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

  - [OSX Build Notes](doc/build-osx.md)
  - [Unix Build Notes](doc/build-unix.md)
  - [Windows Build Notes](doc/build-msw.md)

 
# mingoldcoin.conf
rpcuser=mgcuser
rpcpassword=mgcpassword
listen=1
txindex=1
rpcport=34436
addnode=192.168.193.137
addnode=192.168.193.135
addnode=165.227.124.168
addnode=159.203.111.166

![](http://dogesay.com/wow//////such/coin)

Translations
------------

Changes to translations as well as new translations can be submitted to
[Bitcoin Core's Transifex page](https://www.transifex.com/projects/p/bitcoin/).

Periodically the translations are pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

If the changes are MineGoldCoin specific, they can be submitted as pull request against this repository.
If it is a general translation, consider submitting it through upstream, as we will pull these changes later on.

Development tips and tricks
---------------------------

**compiling for debugging**

Run configure with the --enable-debug option, then make. Or run configure with
CXXFLAGS="-g -ggdb -O0" or whatever debug flags you need.

**debug.log**

If the code is behaving strangely, take a look in the debug.log file in the data directory;
error and debugging message are written there.

The -debug=... command-line option controls debugging; running with just -debug will turn
on all categories (and give you a very large debug.log file).

The Qt code routes qDebug() output to debug.log under category "qt": run with -debug=qt
to see it.

**testnet and regtest modes**

Run with the -testnet option to run with "play minegoldcoins" on the test network, if you
are testing multi-machine code that needs to operate across the internet.

If you are testing something that can run on one machine, run with the -regtest option.
In regression test mode blocks can be created on-demand; see qa/rpc-tests/ for tests
that run in -regest mode.

**DEBUG_LOCKORDER**

MineGoldCoin Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure
CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.
