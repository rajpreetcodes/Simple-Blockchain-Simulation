# Simple Blockchain Simulation

A basic blockchain simulation in Python created to learn the fundamentals of blocks, hashing, mining, and consensus mechanisms.

This project covers:
- Creating a `Block` class and linking blocks into a chain.
- Simulating Proof of Work mining with a nonce.
- Demonstrating how tampering breaks the chain's integrity.
- Simulating PoW, PoS, and DPoS consensus mechanisms.

## Code Files

* `block_simulation.ipynb`: Demonstrates the creation of a basic chain and the effect of tampering.
* `mining_simulation.ipynb`: Simulates the Proof of Work mining process.
* `consensus_simulation.ipynb`: Simulates three different consensus mechanisms.

## Theoretical Assignment

Blockchain Theory Explained
What is a Blockchain?
A blockchain is a decentralized and immutable digital ledger that records transactions in a secure and transparent way. Think of it as a chain of digital blocks, where each block contains a batch of transactions. Each new block is cryptographically linked to the one before it, creating a secure and unbroken chain. Because the ledger is distributed across many computers, it is not controlled by any single entity (it's decentralized) and the data, once written, cannot be altered (it's immutable).

Use Case 1: Cryptocurrency: The most famous use case is for cryptocurrencies like Bitcoin, where the blockchain tracks all transactions without needing a central bank.
Use Case 2: Supply Chain Management: Companies use blockchains to track products from production to sale, ensuring transparency and authenticity.
The Anatomy of a Block
A block is a container for data within the blockchain. Each block consists of two main parts: the header and the body.

Data: The information recorded in the block, such as transaction details.
Hash: A unique, fixed-length "digital fingerprint" of the block's content. It is generated using a hash function.
Previous Hash: The hash of the block that came before it in the chain. This is the crucial link that secures the chain. If the previous block's data is tampered with, its hash will change, and this link will break.
Timestamp: A record of when the block was created.
Nonce: Short for "number used once." It is a random number that miners change repeatedly to find a valid hash during the mining process (Proof of Work).
Merkle Root: A single hash that represents all the transactions within the block. It's like a "fingerprint of all fingerprints," providing a quick and secure way to verify that none of the transaction data in the block has been tampered with.
Consensus Mechanisms
Consensus mechanisms are the rules that a blockchain network uses to agree on the validity of transactions and to add new blocks to the chain.

1. Proof of Work (PoW)
Proof of Work is a consensus mechanism where "miners" compete to solve a complex mathematical puzzle. The first miner to solve the puzzle gets the right to add the next block to the chain and is rewarded with cryptocurrency. This process requires significant computational power, making the network secure but also energy-intensive.

2. Proof of Stake (PoS)
Proof of Stake is an alternative that is more energy-efficient. Instead of miners competing with computing power, users called "validators" lock up (or "stake") their own coins for a chance to be randomly selected to create the next block. The more coins a validator stakes, the higher their chance of being chosen. If a validator approves fraudulent transactions, they lose their staked coins, which creates a strong incentive to act honestly.

3. Delegated Proof of Stake (DPoS)
Delegated Proof of Stake is an evolution of PoS that works like a representative democracy. Coin holders use their stake to vote for a small, fixed number of "delegates" or "witnesses." These elected delegates are responsible for validating transactions and creating new blocks on behalf of the network. This system is very fast and efficient because only a small number of trusted parties need to reach an agreement. Delegates who misbehave can be voted out by the community.
