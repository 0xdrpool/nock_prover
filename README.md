# nock_prover
**Nockchain is a lightweight blockchain for heavyweight verifiable applications. [Drpool](https://drpool.io/)**

## 🚀 Getting Started with Mining 

1. **Download**

    📥 [Download Here](download.md)
    ```sh
    wget https://pub-38955235c3264999bbd95cee1430bad2.r2.dev/image/dr_nock_prover-1.0.5.tar.gz
    ```
2. **Run**
    ```sh
    tar -zxvf dr_nock_prover-x.x.x.tar.gz
    cd dr_nock_prover
    nohup ./nock_prover -p nock.drpool.io:30128 -w drpoolaccount.xxx >> nock.log 2>&1 &
    ```
   
## Currently Supported CPU Models
1. AMD EPYC 7532 32-Core Processor
2. Intel(R) Xeon(R) CPU E5-2650 v4 @ 2.20GHz
3. AMD EPYC 7742 64-Core Processor

## Run  Result
**Test Software:** 1.0.5  
**Virtual Machine:** Yes  
**CPU Model:** AMD EPYC 7532 32-Core Processor  

**Test Procedure:**  
1. Plan to launch 7 CPU cores.  
2. Execution command:  
   ```bash
   nohup taskset -c 0~6 ./nock_prover -p nock.drpool.io:30128 -w xxxx.xxxx >> nock.log 2>&1 &
   ```  

**Test Results:**  
1. **Memory Usage:** ~2GB per process (total ≥14GB required).  
2. **Performance:** ~25 computations completed on average within 5 minutes.  

<img width="1016" height="296" alt="image" src="https://github.com/user-attachments/assets/9a8b4d86-c46b-4973-be3e-4232a60d7320" />
<img width="824" height="241" alt="image" src="https://github.com/user-attachments/assets/482f7c21-b1c5-46db-b9f6-3f4f164c0b28" />
