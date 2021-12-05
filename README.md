# Building a simple blockchain.
 blockchain is an immutable, sequential chain of records called Blocks. They can contain transactions, files or any data you like, really. But the important thing is that they’re chained together using hashes.

 
 
 ## Cahier des charges:
 
### Project Goal:
- Having a functioning Blockchain with a solid grasp.
- How Blockchains work & the fundamental technology behind them.
 
### Project Steps 
## Step 1: Building a Blockchain

We’ll create a Blockchain class whose constructor creates an initial empty list (to store our blockchain), and another to store transactions.Our Blockchain class is responsible for managing the chain. It will store transactions and have some helper methods for adding new blocks to the chain. Let’s start fleshing out some methods.**
**What does a Block look like?
Each Block has an index, a timestamp (in Unix time), a list of transactions, a proof (more on that later), and the hash of the previous Block.**
**Understanding Proof of Work:
A Proof of Work algorithm (PoW) is how new Blocks are created or mined on the blockchain. The goal of PoW is to discover a number which solves a problem. The number must be difficult to find but easy to verify—computationally speaking—by anyone on the network. This is the core idea behind Proof of Work.In Bitcoin, the Proof of Work algorithm is called Hashcash. And it’s not too different from our basic example above. It’s the algorithm that miners race to solve in order to create a new block. In general, the difficulty is determined by the number of characters searched for in a string. The miners are then rewarded for their solution by receiving a coin—in a transaction.**
## Step 2: Our Blockchain as an API
**
We’re going to use the Python Flask Framework. It’s a micro-framework and it makes it easy to map endpoints to Python functions. This allows us talk to our blockchain over the web using HTTP requests.The Mining Endpoint **

** Our mining endpoint is where the magic happens, and it’s easy. It has to do three things:
Calculate the Proof of Work
Reward the miner (us) by adding a transaction granting us 1 coin
Forge the new Block by adding it to the chain
**

## Step 3: Interacting with our Blockchain
 **
 here, we can use plain old cURL or Postman to interact with our API over a network.
 
 **
## Step 4: Consensus
** We’ve got a basic Blockchain that accepts transactions and allows us to mine new Blocks. But the whole point of Blockchains is that they should be decentralized. And if they’re decentralized, how on earth do we ensure that they all reflect the same chain? This is called the problem of Consensus, and we’ll have to implement a Consensus Algorithm if we want more than one node in our network. **

### 




### Remarque:
**l'objectif du projet était de l'héberger dans Microsoft Azure à l'aide d'instances de conteneur(docker&azureWebApp).
malchanceux, il n'a pas pu s'exécuter localement. J'ai déjà beaucoup essayé pour trouver une solution, mais cela n'a pas fonctionné.**
