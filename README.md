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
