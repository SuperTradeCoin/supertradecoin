# MineGoldCoin Core [MGC]
==========================

![MineGoldCoin]()

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


**DEBUG_LOCKORDER**

MineGoldCoin Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure
CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.
