# Bosque-Guardian Token

## Specifications and uses of the BOSQ Utility Token

BOSQ Token version 0.1.0 beta

"BOSQ" is the ticker for the Guardian coin. BOSQ is a utility coin, which gives our users access to the services provided by the Bosque Guardian Foundation. 


## What is a utility token?

A utility token represents access to a future product or service. When you buy a utility token, you are buying your “right” to use a service that’s being developed by a project once it’s finished and launched.

## What rights will I have if I hold the BOSQ utility token?

coming soon

## BOSQ Mainnet Specifications

    Max Supply: 21 Million BOSQ
    Block Time: 1 minute
    Block Reward: 0.00001
    Mining Algorithm: Equihash
    RPCPORT: 22567
    This version of Komodo Independent Chain contains Bitcore support for komodo and all its assetchains.
     

## Guardian Coin Resources

coming soon
    
## About Guardian Coin 
coming soon 


## Getting started
Dependencies
------------
Install Komodo: https://docs.komodoplatform.com/en/latest/komodo/install-Komodo-manually.html#installing-komodo-manually

After installing the Komodo repository, follow the steps:

`cd Komodo/src`

Now run the following command to start the BOSQ chain.  

# Mainnet
`./komodod -ac_name=BOSQ -ac_supply=21500000 -ac_reward=3000000 -ac_pubkey=RPB7YrGuTPCQoHE77sdt1vY9hRKpX8QBHx -addnode=54.39.23.248 -gen &`

Once the BOSQ chain is synched, you are able to use the wallet functionality

# Commands 
In order to perform a command you must navigate to

`cd komodo src`

and execute commands with the following prefix

`./fiat-cli BOSQ`

i.e. Command to get wallet info

`./fiat-cli BOSQ getinfo`

# Main Commands
## Wallet
- getinfo 
- backupwallet "destination"
- dumpprivkey "bosqaddress"
- dumpwallet "filename"
- encryptwallet "passphrase"
- getaccount "BOSQ_address"
- getaccountaddress "account"
- getaddressesbyaccount "account"
- getbalance ( "account" minconf includeWatchonly )
- getnewaddress ( "account" )
- getrawchangeaddress
- getwalletinfo
- importaddress "address" ( "label" rescan )
- importprivkey "komodoprivkey" ( "label" rescan )
- importwallet "filename"
- listaccounts ( minconf includeWatchonly)
- listaddressgroupings
- listlockunspent
- listtransactions ( "account" count from includeWatchonly)
- listunspent ( minconf maxconf  ["address",...] )
- lockunspent unlock [{"txid":"txid","vout":n},...]
- resendwallettransactions
- sendfrom "fromaccount" "toBOSQaddress" amount ( minconf "comment" "comment-to" )
- sendmany "fromaccount" {"address":amount,...} ( minconf "comment" ["address",...] )
- sendtoaddress "BOSQ_address" amount ( "comment" "comment-to" subtractfeefromamount )
- setaccount "BOSQ_address" "account"
- settxfee amount
- signmessage "BOSQ address" "message"

## Zero Knowledge Addresses
- z_exportkey "zaddr"
- z_exportviewingkey "zaddr"
- z_exportwallet "filename"
- z_getbalance "address" ( minconf )
- z_getnewaddress
- z_getoperationresult (["operationid", ... ])
- z_getoperationstatus (["operationid", ... ])
- z_gettotalbalance ( minconf includeWatchonly )
- z_importkey "zkey" ( rescan startHeight )
- z_importviewingkey "vkey" ( rescan startHeight )
- z_importwallet "filename"
- z_listaddresses ( includeWatchonly )
- z_listoperationids
- z_listreceivedbyaddress "address" ( minconf )
- z_mergetoaddress ["fromaddress", ... ] "toaddress" ( fee ) ( transparent_limit ) ( shielded_limit ) ( memo )
- z_sendmany "fromaddress" [{"address":... ,"amount":...},...] ( minconf ) ( fee )
- z_shieldcoinbase "fromaddress" "tozaddress" ( fee ) ( limit )
- zcbenchmark benchmarktype samplecount
- zcrawjoinsplit rawtx inputs outputs vpub_old vpub_new
- zcrawkeygen
- zcrawreceive zcsecretkey encryptednote
- zcsamplejoinsplit

## Blockchain
- getbestblockhash
- getblock "hash|height" ( verbose )
- getblockchaininfo
- getblockcount
- getblockhash index
- getblockhashes timestamp
- getblockheader "hash" ( verbose )
- getdifficulty
- getspentinfo

## Control 
- getinfo
- help ( "command" )
- stop

## Generating
- generate numblocks
- getgenerate
- setgenerate generate ( genproclimit )

## Network
- addnode "node" "add|remove|onetry"
- clearbanned
- getconnectioncount
- getdeprecationinfo
- getnettotals
- getnetworkinfo
- getpeerinfo
- listbanned
- ping
- setban "ip(/netmask)" "add|remove" (bantime) (absolute)

## For all commands type the following
```
cd komodo/src
./komodo-cli -ac_name=BOSQ help
```

Deprecation Policy
------------------

This release is considered deprecated one year after the release day. There
is an automatic deprecation shutdown feature which will halt the node some
time after this one year period. The automatic feature is based on block
height and can be explicitly disabled.


**Komodo is unfinished and highly experimental, use at your own risk.**


**To change modes:**

a) backup all privkeys (launch komodod with `-exportdir=<path>` and `dumpwallet`)

b) start a totally new sync including `wallet.dat`, launch with same `exportdir`

c) stop it before it gets too far and import all the privkeys from a) using `komodo-cli importwallet filename`

d) resume sync till it gets to chaintip

For example:
```shell
./komodod -exportdir=/tmp &
./komodo-cli dumpwallet example
./komodo-cli stop
mv ~/.komodo ~/.komodo.old && mkdir ~/.komodo && cp ~/.komodo.old/komodo.conf ~/.komodo.old/peers.dat ~/.komodo
./komodod -exchange -exportdir=/tmp &
./komodo-cli importwallet /tmp/example
```

License
-------
For license information see the file [COPYING](COPYING).

