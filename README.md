# MineGoldCoin Core [MGC]
==========================
## What is MineGoldCoin? 
MineGoldCoin is a cryptocurrency like Bitcoin, although it does not use SHA256 as its proof of work (POW). Taking development cues from Tenebrix and Litecoin, MineGoldCoin currently employs a simplified variant of scrypt.

https://minegoldcoin.com/

 - Currency unit : MGC
 - Algorithm : Scrypt
 - Block Interval : 1 minute (60 seconds)
 - Difficulty Retarget : Every block (using Kimoto's Gravity Well)
 - Total coins amount : 25,000,000 MGC
Block reward 
 - Premine: First 10 block are 2,500,000 MGC 
 - Bonus reward for block 11 to 10,000 of 3.5 coins
 - Bonus reward for block 10,000 - 100,000 of 5 coins
 - Bonus reward for block 100,000 - 400,000 of 15 coins
 - Bonus reward for block 400,000 - 1,200,000 of 20 coins
 - Subsidy is cut in half every 400,000 blocks starting at block 1600000
 - Premine : None
 
  
### Overview plz make minegoldcoind/minegoldcoin-cli/minegoldcoin-qt

  The following are developer notes on how to build MineGoldCoin on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

  - [OSX Build Notes](doc/build-osx.md)
  - [Unix Build Notes](doc/build-unix.md)
  - [Windows Build Notes](doc/build-msw.md)

 
# minegoldcoin.conf
  - rpcuser=mgcuser
  - rpcpassword=mgcpassword
  - listen=1
  - txindex=1
  - rpcport=34436
  - port=34437
  - addnode=192.168.193.137
  - addnode=192.168.193.135
  - addnode=165.227.124.168
  - addnode=159.203.111.166
  - addnode=199.192.16.144
  - addnode=199.192.16.129 


**DEBUG_LOCKORDER**

MineGoldCoin Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure
CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.
