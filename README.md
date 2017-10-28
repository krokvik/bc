# proof-of-sport

> Smart contract for hackaton

## How to start test network:

#### Install Geth
- [Ubuntu](https://github.com/ethereum/go-ethereum/wiki/Installation-Instructions-for-Ubuntu)
- [MacOS](https://github.com/ethereum/go-ethereum/wiki/Installation-Instructions-for-Mac)

#### Install Mist
https://github.com/ethereum/mist/releases

#### Do the magic

``` bash
# start geth test network
geth --dev --rpccorsdomain "*" --rpc --rpcaddr "localhost" --networkid 8545 --minerthreads "1" --rpcapi  "admin,debug,miner,shh,txpool,personal,eth,net,web3" console

# in Geth console create new account
personal.newAccount("<put_password_here>")

# open Mist wallet with parameters regarding your test network
# Mac:
/Applications/Mist.app/Contents/MacOS/Mist --rpc http://localhost:8545
# Ubuntu:
/usr/bin/mist --rpc http://localhost:8545
```

After this - deploy smart contract **sportcoin.sol** from "smart_contracts" folder. Now you are ready to use your contracts!
