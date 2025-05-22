# nock_prover
**Nockchain is a lightweight blockchain for heavyweight verifiable applications. [Drpool](https://drpool.io/)**

## 🚀 Getting Started with Mining （Solo）

1. **Download**

    📥 [Download Here](download.md)

   ubuntu
    ```
    wget https://pub-38955235c3264999bbd95cee1430bad2.r2.dev/image/ubuntu-nockchain-1.0.0.tar.gz
    ```
    mac
    ```
    wget https://pub-38955235c3264999bbd95cee1430bad2.r2.dev/image/macos-nockchain-1.0.0.tar.gz
    ```

3. **Extract & Prepare**

    ubuntu
    ```sh
    tar -zxvf ubuntu-nockchain-1.0.0.tar.gz && cd script
    ```
    mac
    ```sh
    tar -zxvf macos-nockchain-1.0.0.tar.gz && cd script
    ```

5. **Create Wallet**
    ```sh
    # generate new wallet
    ./generate-wallet.sh
    ```
    log
    ```txt
    🔐 Generating wallet keys...
    🔑 New Wallet Keys: 
    Public Key:  42dbukjpyD***vMie36Vo9g3Cpnkpw4
    Private Key: LqtY4huH***nz78iJCJh
    Memo:        crew *** suggest
    ```

6. **Start**
    ```sh
    # Run nockchain mainnet
    ./start mainnet
    ```

7. **View logs**
    ```sh
    tail -f mainnet.log
    ```

## ​Transitional arrangement​

1. stop mining
```
./stop.sh
```

2. Update `mainnet.sh` file contents
```sh
#!/bin/bash

pids=$(ps -ef | grep ../nockchain | grep -v grep | awk '{print $2}')
if [ -n "$pids" ]; then
    echo "$pids" | xargs kill
    sleep 5
fi
MINING_PUBKEY=$1

[ ! -d "miner-node" ] && mkdir miner-node
cd miner-node
rm -f nockchain.sock

while true; do
    target=$(ps aux | grep ../nockchain | grep -v grep)
    if [ -z "$target" ]; then
        export RUST_LOG=info && ../nockchain --npc-socket nockchain.sock --mining-pubkey $MINING_PUBKEY --mine --bind /ip4/0.0.0.0/udp/3006/quic-v1 --peer /ip4/95.216.102.60/udp/3006/quic-v1 --peer /ip4/65.108.123.225/udp/3006/quic-v1 --peer /ip4/95.216.102.60/udp/3006/quic-v1 --peer /ip4/65.108.123.225/udp/3006/quic-v1 --peer /ip4/65.109.156.108/udp/3006/quic-v1 --peer /ip4/65.21.67.175/udp/3006/quic-v1 --peer /ip4/65.109.156.172/udp/3006/quic-v1 --peer /ip4/34.174.22.166/udp/3006/quic-v1 --peer /ip4/34.95.155.151/udp/30000/quic-v1 --peer /ip4/34.18.98.38/udp/30000/quic-v1
        sleep 5
    fi
    sleep 60
done
```
3. restart mining
```
./start.sh mainnet
```
