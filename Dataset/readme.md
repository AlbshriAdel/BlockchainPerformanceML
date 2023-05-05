# Blockchain Data Analysis and Performance Prediction

@author: Adel Albishri

This file contains a description of the blockchain data generated from a simulator for the purpose of predicting the performance of a blockchain system. We ran the simulator 184 times with different configurations to have a dataset that can be split into training and testing. The data file contains several sheets. A detailed description is as follows:
  
## Contents

1. [Config sheet](#config-sheet)
2. [Results sheet](#results-sheet)
3. [Block sheet](#block-sheet)
4. [Transaction sheet](#transaction-sheet)
5. [TransactionLatency sheet](#transactionlatency-sheet)
6. [TransactionPool sheet](#transactionpool-sheet)

### Config sheet

Each row in this file contains a description of the input parameter values used for configuring one simulation run. These used parameters are:

- No. of Nodes: This is an integer feature that represents the number of the involved nodes.
- No. of Miner: This is an integer feature that represents the number of the involved miner nodes. Throughout the data, we can notice that this is set to 1. The reason behind this is the usage of the Raft consensus algorithm which restricts the number of miner nodes to 1.
- Consensus Algorithm: This is a categorical feature whose values represent the name of the consensus algorithm used.
- Total No of Transactions Per Sec: This is an integer feature representing the total number of transactions the system can generate in one second.
- Max Block Size: This is an integer feature representing the maximum allowed block size in MB.
- Max Tx Size: This is a numerical feature representing the maximum allowed transaction size in MB.
- Min Tx Size: This is a numerical feature representing the minimum allowed transaction size in MB.
- Block Interval: This is a numerical feature representing the interval for the generated blocks.

### Results sheet

Each row in this file contains a description of the output metrics resulted from configuring the simulator with the values in the corresponding row in the config sheet. The used metrics are:

- Total No. of Blocks: This is an integer feature that represents the number of generated blocks in the run.
- Total No. of Blocks include Tx: This is an integer feature that represents the number of generated blocks containing transactions in the run.
- Total No. of Blocks without Tx: This is an integer feature that represents the number of generated blocks that do not contain transactions in the run.
- Avg. Block Size (MB): This is a numerical feature representing the average size of the generated blocks in the run.
- Total No of Transactions: This is an integer feature that represents the number of generated transactions in the run.
- Avg. No. of Tx per block: This is a numerical feature representing the average number of transactions in the generated blocks in the run.
- Avg. of Tx Inclusion Time (secs): This is a numerical feature representing the average time taken for the transaction to be included in a block in the run.
- Avg. Tx Size (MB): This is a numerical feature representing the average size of transactions in the run.
- Total No. of Pending Tx: This is an integer feature that represents the number of pending transactions at the end of the run.
- Avg. Block Propagation (secs): This is a numerical feature representing the average time taken for the block to be propagated over the nodes.
- Avg. Transaction Latency (secs): This is a numerical feature representing the average latency time for the transaction.
- Transactions execution (secs): This is a numerical feature representing the average time taken for the transaction to be executed in the run.
- Transaction Throughput (Tx/secs): This is a numerical feature representing the throughput time taken by the transaction.

### Block sheet

Each raw in this sheet gives detailed description of the generated block in a corresponding run. The included features are:

-	Simulator No. Run: this is integer feature that represents the run number in which the block is generated.
-	Block ID: this is integer feature that represents the number of the block in the run.
-	Previous Block ID: this is integer feature that represents the number of previous block in the run.
-	Block Depth: this is integer feature that represents the block’s depth.
-	Block Timestamp: this is numerical feature representing the block’s timestamp.
-	Block Size: this is numerical feature representing the block size in the run.
-	No. of Transactions: this is integer feature that represents the number of transactions included in the block.
-	Mined by: this is integer feature that represents the number of miner node that mined such block.
-	Transaction sheet: Each raw in this sheet gives detailed description of the generated transaction in a corresponding run. The included features are:
-	Simulator No. Run: this is integer feature that represents the run number in which the transaction is generated.
-	Transaction ID: this is integer feature that represents the transaction ID.
-	Creation time: this is integer feature that represents the time where the transaction is created.
-	Confirmation time: this is integer feature that represents the time where the transaction is confirmed.
-	Transaction size: this is integer feature that represents the transaction size in MB.
-	Block ID: this is integer feature that represents the block number in which the transaction is included.

### TransactionLatency sheet

Each raw in this sheet gives the latency data for a transaction. The used features are:

-	Simulator No. Run: this is integer feature that represents the run number in which the transaction is generated.
-	Transaction ID: this is integer feature that represents the transaction ID.
-	Creation time: this is integer feature that represents the time where the transaction is created.
-	Confirmation time: this is integer feature that represents the time where the transaction is confirmed.
-	Transaction Latency: this is integer feature that represents the latency time for the transaction. 

### TransactionPool sheet 

Each raw in this sheet represents the status of the transaction on the pool. The used features are:

-	Simulator No. Run: this is integer feature that represents the run number in which the transaction is generated.
-	Transaction ID: this is integer feature that represents the transaction ID.
-	Creation time: this is integer feature that represents the time where the transaction is created.
-	Transaction size: this is integer feature that represents the transaction size in MB.
-	Status: this is a categorical feature representing the transaction status in the pool.
