# docker-eth-demo

Run a public Ethereum testnet

https://medium.com/@mattlovan/run-a-public-ethereum-testnet-f0e40cefc1f2

Running two ethreum testnet on two different docker network, `chain1` and `chain2`.

On each cain, there are three nodes:
- miner{1|2}
  miner node
- publicnode{1|2}
  Nodes bootratped by miner node. it exposes json-rpc port at 18545 & 28545.
- netstats{1|2}
  status ui
  check http://localhost:1300 & http://localhost:2300 for chian1 and chain2, respectively.

## genesis
In both network 
account 0x66414e903305Ff1E9dD8266AEDb359A9773236FC are allocated with 
100000000000000000000000 wei (100000 ether)

For the details check, `monitored-geth-client/files/genesis.json` direcotry.

## chain parameters
- chain1
    chain id: 654321
- chain2
    chain id: 654322

# HOWTO
- spin up
`docker-compose up -d`

tested on

docker-compose version 1.27.4, build unknown

Linux 5.13.0-28-generic #31-Ubuntu SMP


#TODO
- use different nodeid
- use different seed account

