# proof-of-sport

> Smart contract for hackaton

## How to start test network:

#### Install Geth
- [Ubuntu](https://github.com/ethereum/go-ethereum/wiki/Installation-Instructions-for-Ubuntu)
- [MacOS](https://github.com/ethereum/go-ethereum/wiki/Installation-Instructions-for-Mac)

#### Install Mist or Ethereum Wallet (better Ethereum Wallet)
https://github.com/ethereum/mist/releases

#### Do the magic

``` bash
# start geth test network
geth --dev --rpccorsdomain "*" --rpc --rpcaddr "localhost" --networkid 8545 --minerthreads "1" --rpcapi  "admin,debug,miner,shh,txpool,personal,eth,net,web3" console

# in Geth console create new account
personal.newAccount("<put_password_here>")

# open Mist wallet with parameters regarding your test network
# Mac:
open -a "Ethereum Wallet.app" --args --rpc http://0.0.0.0:8545
# Ubuntu:
ethereumwallet —rpc http://localhost:8545
```

After this - deploy smart contract **sportcoin.sol** from "smart_contracts" folder. Now you are ready to use your contracts!

#### How to mine in geth console:

``` bash
# start mining
miner.start();

# stop mining
miner.stop()
```
