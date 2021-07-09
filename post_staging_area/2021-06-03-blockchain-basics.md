---
layout: post
category: reviews
---

Welcome to Part-1 of my blog series on the basics of blockchains. It's no surprise that blockchains and cryptocurrencies have been all the buzz for a while now and I really wanted to understand what's more to blockchains than just the buzz words. I've only taken baby steps so far but my first serious attempt at learning was when I took the course- Blockchain Basics on Coursera[^2]. This blog series is my attempt to explain what I've learned from this course and additional research I did on the topic.

<script type="text/javascript" src="https://files.coinmarketcap.com/static/widget/coinPriceBlock.js"></script><div id="coinmarketcap-widget-coin-price-block" coins="1,1027,825,74" currency="USD" theme="light" transparent="false" show-symbol-logo="true"></div>
##### Latest prices of some popular cryptocurrencies. [^1]

## Table of contents
- [Blockchain Structure](#blockchain-structure)
- [Basic Operations](#basic-operations)
- [What are Smart Contracts?](#smart-contracts)
- [Another Blockchain- Ethereum](#ethereum)
- [Incentive Model](#incentive-model)
- [Cryptography and Hashing](#cryptography-and-hashing)
- [Decentralization](#decentralization)
- [Consensus Protocols](#consensus-protocols)
- [Robustness](#robustness)
- [Forks](#forks)

## [Blockchain Structure](#blockchain-structure)

Blockchain is a store of information (ledger) that is stored not in a centralized server or group of servers but on a multitude of computing devices called nodes that each have a copy of this blockchain. The blockchain itself consists of a chain of linked blocks where each block is a package of transactions along with some other metadata that helps identify the block and its location within the blockchain. As transactions happen in the network, new blocks get created and are added to the blockchain. This is how the blockchain grows. The nodes play a crucial role in processing transactions, creating and validating blocks and maintaining the integrity of the blockchain or distributed ledger It is near impossible to make any fraudulent changes to the blockchain because any change would have to be replicated across tens of thousands of copies of the blockchain near-instantly all while the blockchain is growing. This requires a practically impossible amount of computing power.

![Bitcoin Blockchain Structure](https://adikamath.github.io/assets/images/2021-06-03-blockchain-basics/Bitcoin_Block_Data.png)
##### Basic structure of a Bitcoin blockchain[^3]

As you can see from the image above, the blockchain is a chain of blocks whereby each block is linked to the previous block. At a high-level, here are the core components of a Bitcoin block[^4]:

| Block Component     | Description                                               |
|---------------------|-----------------------------------------------------------|
| Size                | The size of all elements contained in the block in bytes. |
| Header              | A collection of important metadata.                       |
| Transaction Counter | Total number of transactions contained within the block.  |
| Transactions        | The list of all transactions.                             |

And here we look closer at what makes up a block header[^5]:

| Header Component    | Description                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version             | A version number that is current to the software upgrade of the network/protocol.                                        |
| Previous Block Hash | The hash pointing to the previous or parent block of the current block in the blockchain.                                |
| Merkle Root Hash    | The hash generated based on the current transactions listed in the current block.                                        |
| Timestamp           | The timestamp of when the block was created.                                                                             |
| Difficulty Target   | The difficulty level of the puzzle to be solved for this block.                                                          |
| Nonce               | Abbreviation for "Number used only once"- the number/ answer to the puzzle that the miners have to solve for this block. |

You can search for and explore any bitcoin block here: bitcoin.com/blockexplorer.


## [Basic Operations](#basic-operations)

Take the Bitcoin blockchain- it is essentially made up of transactions! For example, Person A sends a transaction to Person B and once this transaction is validated and completed, it is added to the blockchain where it remains forever. This is how blockchains grow in essence. In the Bitcoin blockchain, transactions are created using something called an Unspent Transaction Output or UTXO. A UTXO is the store of value that represents a fixed monetary amount. The total amount of Bitcoin you have available for spending is the sum of all unspent UTXOs in your wallet. And UTXOs in your wallet are created either when you receive a transaction from someone else or by mining Bitcoin. Let's now look at the steps that take place when a transaction is initiated:

| Step                     | Description                                                                                                                                                                                                                                                                                                                                                |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wallet                   | UTXOs are present in the wallet/ wallets for use in the transaction.                                                                                                                                                                                                                                                                                       |
| Transaction Generation | The user creates the transaction providing the client application the necessary details like recipient's wallet address and amount to be sent. The transaction is signed with the user's private keys.                                                                                                                                                     |
| Broadcast                | The transaction is broadcast through the closest node in the network. The node broadcasts the transaction to other nodes in the network who do the same and the transaction propagates through the network.                                                                                                                                                |
| Verification             | Basic details of the transaction are verified by the nodes like the user's signature, if the sender of the transaction has enough inputs to make the transaction (preventing double-spend), the structure of the transaction, etc.                                                                                                                         |
| Memory Pool              | The verified transaction makes it's way to a pool of unconfirmed transactions called "Mempool" short for memory pool. At this point, the transaction is still not part of the blockchain.                                                                                                                                                                  |
| Mining & Validation      | The transaction is scooped up by a miner (preference is given to transactions paying the highest fees) and added to a block creating with other transactions. Once the block is created the miner solves a puzzle to add the block to the blockchain. After solving the puzzle, the block is added to the blockchain and broadcasted through the network.  |
| Confirmation             | After the block with the transaction is added to the blockchain and broadcasted, the user receives the first transaction confirmation. As more blocks are added to the blockchain, the transaction is referenced in these blocks and after 6 confirmations, the transaction is considered to be safely validated.                                          |


## [What are Smart Contracts?](#smart-contracts)



## [Another Blockchain- Ethereum](#ethereum)

Fusce non velit cursus ligula mattis convallis vel at metus. Sed pharetra tellus massa, non elementum eros vulputate non. Suspendisse potenti. Quisque arcu felis, laoreet vel accumsan sit amet, fermentum at nunc. Sed massa quam, auctor in eros quis, porttitor tincidunt orci. Nulla convallis id sapien ornare viverra. Cras nec est lacinia ligula porta tincidunt. Nam a est eget ligula pellentesque posuere. Maecenas quis enim ac risus accumsan scelerisque. Aliquam vitae libero sapien. Etiam convallis, metus nec suscipit condimentum, quam massa congue velit, sit amet sollicitudin nisi tortor a lectus. Cras a arcu enim. Suspendisse hendrerit euismod est ac gravida. Donec vitae elit tristique, suscipit eros at, aliquam augue. In ac faucibus dui. Sed tempor lacus tristique elit sagittis, vitae tempor massa convallis.

## References

[^1]: [CoinMarketCap.Com](https://www.coinmarketcap.com)
[^2]: [Blockchain Basics- Coursera](https://www.coursera.org/learn/blockchain-basics)
[^3]: [Matthäus Wander, CC BY-SA 3.0, via Wikimedia Commons](<https://creativecommons.org/licenses/by-sa/3.0>)
[^4]: [Block Structure, via Bitcoin Wiki](https://en.bitcoin.it/wiki/Block)
[^5]: [A Decomposition Of The Bitcoin Block Header](https://www.datadriveninvestor.com/2019/11/21/a-decomposition-of-the-bitcoin-block-header/)
