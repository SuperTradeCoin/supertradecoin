# SuperTradeCoin Core [SPTDC]
==========================
## What is SuperTradeCoin? 
SuperTradeCoin is a cryptocurrency like Bitcoin, although it does not use SHA256 as its proof of work (POW). Taking development cues from Tenebrix and Litecoin, SuperTradeCoin currently employs a simplified variant of scrypt.
 
https://www.supertradecoin.com/

 - Currency unit : SPTDC
 - Algorithm : Scrypt
 - Block Interval : 1 minute (60 seconds)
 - Difficulty Retarget : Every block (using Kimoto's Gravity Well)
 - Total supply : 25,000,000,000 SPTDC
Block reward 
 - Premine: First 10 block are 2,500,000,000 SPTDC  
 - Bonus reward for block 11 to 299999 of 1000 coins       
 - Bonus reward for block 299999 - 399999 of 500 coins              
 - Bonus reward for block 399999 - 599999 of 250 coins         
 - Bonus reward for block 599999 - 1,000,000 of 100 coins    
 - Subsidy is cut in half every 200,000 blocks starting at block 1200000
 
  
### Overview plz make supertradecoind/supertradecoin-cli/supertradecoin-qt

  The following are developer notes on how to build SuperTradeCoin on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

  - [OSX Build Notes](doc/build-osx.md)
  - [Unix Build Notes](doc/build-unix.md)
  - [Windows Build Notes](doc/build-msw.md)

 
# supertradecoin.conf
  - rpcuser=sptdcuser
  - rpcpassword=sptdcpassword
  - listen=1
  - txindex=1
  - rpcport=46636
  - port=46637



**DEBUG_LOCKORDER**

SuperTradeCoin Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure
CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.
