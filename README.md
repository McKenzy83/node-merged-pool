High performance Stratum poolserver in Node.js. One instance of this software can startup and manage multiple coin
pools, each with their own daemon and stratum ports :)

#### Notice
I am trying to make this useable software. On my list of up-front todos:

* Multiple PoWAUX coins on each main chain
* Profit Switching

Frontend and payment enhancements will be a separate repo. (Insert repo URL when created)

[![Build Status](https://travis-ci.org/sigwo/node-merged-pool.png?branch=master)](https://travis-ci.org/sigwo/node-merged-pool)

#### Why
The software that I forked was a wonderful beginning that never cvame to fruition. I hope to bring Node stratum into the
mainstream of merged mining.

Features
----------------------------------
* Merged Mining Support
* Daemon RPC interface
* Stratum TCP socket server
* Block template / job manager
* P2P to get block notifications as peer node
* Optimized generation transaction building
* Connecting to multiple daemons for redundancy
* Process share submissions
* Session managing for purging DDoS/flood initiated zombie workers
* Auto ban IPs that are flooding with invalid shares
* __POW__ (proof-of-work) & __POS__ (proof-of-stake) support
* Transaction messages support
* Vardiff (variable difficulty / share limiter)
* When started with a coin daemon that hasn't finished syncing to the network it shows the blockchain download progress and initializes once synced

#### Hashing algorithms supported:
* ✓ __SHA256__ (Bitcoin, Freicoin, Peercoin/PPCoin, Terracoin, etc..)
* ✓ __Scrypt__ (Litecoin, Dogecoin, Feathercoin, etc..)
* ✓ __Scrypt-Jane__ (YaCoin, CopperBars, Pennies, Tickets, etc..)
* ✓ __Scrypt-N__ (Vertcoin [VTC])
* ✓ __Quark__ (Quarkcoin [QRK])
* ✓ __X11__ (Darkcoin [DRK], Hirocoin, Limecoin)
* ✓ __X13__ (MaruCoin, BoostCoin)
* ✓ __NIST5__ (Talkcoin)
* ✓ __Keccak__ (Maxcoin [MAX], HelixCoin, CryptoMeth, Galleon, 365coin, Slothcoin, BitcointalkCoin)
* ✓ __Skein__ (Skeincoin [SKC])
* ✓ __Groestl__ (Groestlcoin [GRS])

May be working (needs additional testing):
* ? *Blake* (Blakecoin [BLC])
* ? *Fugue* (Fuguecoin [FC])
* ? *Qubit* (Qubitcoin [Q2C], Myriadcoin [MYR])
* ? *SHAvite-3* (INKcoin [INK])

Not working currently:
* *Groestl* - for Myriadcoin
* *Keccak* - for eCoin & Copperlark
* *Hefty1* (Heavycoin [HVC])


Requirements
------------
* Node v0.10+
* Coin daemon for primay and auxillery coins (preferably one with a relatively updated API and not some crapcoin :p)
* Patience :)

Example Usage
-------------

#### Install as a node module by cloning repository

```bash
git clone https://github.com/sigwo/node-merged-pool
cd node-merged-pool
npm update
```

Note to self: Add actual instructions here.

#### Module usage

Please see the included example.js file for more information. This section will be
expanded soon.

Credits
-------
* [zone117x](//github.com/zone117x) - Head developer of the original stratum mining pool for node.js
* [vekexasia](//github.com/vekexasia) - co-developer & great tester
* [LucasJones](//github.com/LucasJones) - got p2p block notify working and implemented additional hashing algos
* [TheSeven](//github.com/TheSeven) - answering an absurd amount of my questions, found the block 1-16 problem, provided example code for peer node functionality
* [pronooob](https://dogehouse.org) - knowledgeable & helpful
* [Slush0](//github.com/slush0/stratum-mining) - stratum protocol, documentation and original python code
* [viperaus](//github.com/viperaus/stratum-mining) - scrypt adaptions to python code
* [ahmedbodi](//github.com/ahmedbodi/stratum-mining) - more algo adaptions to python code
* [steveshit](//github.com/steveshit) - ported X11 hashing algo from python to node module
* [KillerByte](//github.com/KillerByte) - for beginning this creation

Donations
---------
Below is my donation address. The original dev addresses are listed because I felt scammy if I removed them. They no longer are supporting the current development
effort. Please donate to:

* BTC: '1BRUcdAdjdQoAgUwcN7nbNDzqhL92ub3xE'
* Cryptsy Trade Key: '197f17af3751709b2c7f076a2d3393e064022e91'


Original author (zone117x):

* BTC: `1KRotMnQpxu3sePQnsVLRy3EraRFYfJQFR`
* LTC: `LKfavSDJmwiFdcgaP1bbu46hhyiWw5oFhE`
* VTC: `VgW4uFTZcimMSvcnE4cwS3bjJ6P8bcTykN`
* MAX: `mWexUXRCX5PWBmfh34p11wzS5WX2VWvTRT`
* QRK: `QehPDAhzVQWPwDPQvmn7iT3PoFUGT7o8bC`
* DRK: `XcQmhp8ANR7okWAuArcNFZ2bHSB81jpapQ`
* DOGE: `DBGGVtwAAit1NPZpRm5Nz9VUFErcvVvHYW`
* Cryptsy Trade Key: `254ca13444be14937b36c44ba29160bd8f02ff76`

License
-------
Released under the GNU General Public License v2

http://www.gnu.org/licenses/gpl-2.0.html
