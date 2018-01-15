# RCoin

RCoin is a decentralized peer-to-peer currency building upon the ideas of Bitcoin. The latest version, RCoinX, is a CryptoNote based cryptocurrency that I'm sure you'll find is convenient and great to use. RCoin is designed to be ASIC resistant by requiring relatively
large amounts of memory per hash.

**News: We have switched to TkWallet3X from TkWallet2X -- should fix issues on Windows 10**

**News: Wallet binaries moved to new CDN**

**News: We have an IRC channel: ##ronsor on irc.freenode.net - [WebChat](http://kiwiirc.com/client/irc.freenode.net/##ronsor)**

**News: [We need more seed nodes. Click here to apply.](https://github.com/tinyrcoin/tkwallet/issues/1)**

## Latest Version

The current version is RCoinX 1.1.

## Features and Information

* RCoin uses the CryptoNight hashing algorithm.
* Block time is 10 seconds.
* Solo-mining is feasible.
* Anonymous message system.

### Anonymous Message System

The anonymous message system allows you to send an anonymous message to anyone with the TkWallet software. The receiver will not know who sent the message, so you will need to find some other way to identify yourself to the recipient (if you so choose). An anonymous message costs only the network fee to send (about 0.0001 RCoin).

## Obtain The Wallet

The RCoin wallet can be downloaded from links below:

* Source Code: see below
* [Windows 64-bit Binaries](https://rcoin.surge.sh/wallet3x-win64.zip) \*(note)

Note: We have switched to TkWallet3x. Wallets cannot be imported from TkWallet2x -- you must transfer all your funds to the new wallet.
TkWallet3X is compatible with command line simplewallet wallets. TkWallet3X can run alongside TkWallet2X. Need to recover funds from an old TkWallet2X wallet? Download the last TkWallet2X version [here](https://rcoin.surge.sh/wallet-win64.zip). TkWallet2X anonymous messages are incompatible with new TkWallet3x anonymous messages.

A standard [Forknote](http://forknote.net) client may be used, provided you have the RCoin configuration file: [coin.conf](https://github.com/tinyrcoin/tkwallet/raw/master/coin.conf).

### Source Code

RCoin currently is based on Forknote. You may obtain our approved copy of the source tree [here](http://github.com/tinyrcoin/forknote). Compiling this will provide you with the command line wallet and daemon. You will need the RCoin "coin.conf" config file, which is available in the [TkWallet3X Repository](https://github.com/tinyrcoin/tkwallet).

If you want the GUI wallet (which you likely do), please check the TkWallet3X Repository -- link provided above.

## Block Explorer

Currently offline.

## FAQ

1. What about the old RCoin?
   > The old RCoin had various issues, from not working at all to too much inflation.
   
2. What's TkWallet?
   > TkWallet (and it's current version, TkWallet3X) is the GUI wallet software that was designed for RCoin.
   
3. How do I mine?
   > If you are using TkWallet, you may mine by going to the "Mining" menu and selecting "Launch Miner", which will start the miner for your current address.
   > If you want to mine for another address, want more control, or are not using TkWallet, you can manually start the miner:
   `./miner --address (address) --threads (number of threads/CPU cores to use) --log-level 4 --daemon-rpc-port 12991` or just see `./miner --help` for all options.
   > See also *Mining Pools*
4. What about a GPU miner?
   > In RCoinX's early stage, a GPU miner would increase difficulty and make it hard for people to CPU mine it. It is not in anyone's interest to start GPU mining early on.
   
5. ASIC mining?
   > Did you even read the first sentence!?!
   
### FAQ: What are the mining pools?

We have three mining pools, unfortunately all of them are not working right now (!):

* [RCoinX Chain Miner](http://rcoinx.chain-miner.com/)
* [LAB Binary Mining](http://labbinarymining.com/)
* [XRX.easygarlic.net](https://xrx.easygarlic.net/)

## Roadmap

- [x] Release RCoinX 1.0
- [-] Get on at least one exchange. (pending)
- [ ] Finish block explorer. 
- [ ] Add lightweight wallet support (like Electrum for Bitcoin).
- [!] Improve anonymous message system. (rewriting)
