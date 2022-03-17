This is the binary release repository for Novo Bitcoin.

## Supported OS

* debian (>= 10.11)
* ubuntu (>= 20.04)

## Node

Including `novobitcoind` & `novobitcoin-cli`

### Node configuration

`~/.novo-bitcoin/novo.conf` example:

```
port=8666
rpcport=8665
rpcuser=USERNAME
rpcpassword=PASSWORD
```

### Start node

    novobitcoind -daemon

## Miner

`novominer` is the mining program.

### Miner dependencies

    apt install libjansson4 libcurl4

### Miner configuration

`cfg.json` example:

```
{
    "url" : "http://127.0.0.1:8665",
    "user" : "USERNAME",
    "pass" : "PASSWORD",
    "algo" : "sha256dt",
    "threads" : "1",
    "coinbase-addr": "1M9uLiL695r9pSxmxgmEUeZD8MXRtCEeJk",
    "quiet" : true
}
```

### Start miner

    novominer -c cfg.json

## Dockerfile

Produce your own docker image with the `Dockerfile`.
