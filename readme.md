## Supported OS

* debian (>= 10.11)
* ubuntu (>= 20.04)

## Node

### Node configuration

`~/.novo-bitcoin/novo.conf` example:

```
port=8666
rpcport=8665
rpcuser=USERNAME
rpcpassword=PASSWORD
```

### Start node

    $ novobitcoind -daemon

### Stop node

    $ novobitcoin-cli stop

## Miner

### Miner dependencies

    $ apt install libjansson4 libcurl4

### Miner configuration

`cfg.json` example:

```
{
    "url" : "http://127.0.0.1:8665",
    "user" : "USERNAME",
    "pass" : "PASSWORD",
    "algo" : "sha256dt",
    "threads" : "1",
    "coinbase-addr": "BITCOIN_ADDRESS"
}
```

**BITCOIN_ADDRESS**:

    $ novobitcoin-cli getnewaddress
    1NBCnKZ93kSaXxiHzXQV4iqUSH4iRSDPmF

### Start miner

    $ novominer -c cfg.json

## Novo Bitcoin wallet

    $ novobitcoin-cli getbalance
    100.0000

    $ novobitcoin-cli sendtoaddress 1NBCnKZ93kSaXxiHzXQV4iqUSH4iRSDPmF 10.0000

## Docker

    $ docker build -t novo-bitcoin:0.1.0 .
