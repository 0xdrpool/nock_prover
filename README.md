# nock_prover
**Nockchain is a lightweight blockchain for heavyweight verifiable applications. [Drpool](https://drpool.io/)**

## 🚀 Getting Started with Mining

1. **Download**

    📥 [Download Here](download.md)
    ```
    # ubuntu
    wget https://pub-38955235c3264999bbd95cee1430bad2.r2.dev/image/ubuntu-nockchain-x=0.1.0.tar.gz

    # mac
    wget https://pub-38955235c3264999bbd95cee1430bad2.r2.dev/image/macos-nockchain-0.1.0.tar.gz
    ```

2. **Extract & Prepare** 
    ```sh
    # ubuntu
    tar -zxvf ubuntu-nockchain-0.1.0.tar.gz && cd script

    # mac
    tar -zxvf macos-nockchain-0.1.0.tar.gz && cd script
    ```

3. **Create Wallet**
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

4. **Start**
    ```sh
    # Run nockchain mode in leader mode
    ./start leader

    # Run nockchain mode in follower mode
    ./start follower

    # Run nockchain mode leader & follower
    ./start leader follower
    ```

5. **View logs**
    ```sh
    # leader mode log
    tail -f leader.log

    # follower mode log
    tail -f follower.log
    ```
