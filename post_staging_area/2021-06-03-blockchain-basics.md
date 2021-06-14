---
layout: post
category: reviews
---

It is no surprise that blockchains and cryptocurrencies have been the talk of the town for a while now and I really wanted to understand what's more to blockchains than just the buzz words.

<script type="text/javascript" src="https://files.coinmarketcap.com/static/widget/coinPriceBlock.js"></script><div id="coinmarketcap-widget-coin-price-block" coins="1,1027,825,74" currency="USD" theme="light" transparent="false" show-symbol-logo="true"></div>
##### Latest prices of some popular cryptocurrencies. [^1]

I've only taken baby steps so far but I came across this course- Blockchain Basics on Coursera that opened my eyes to the technology beyond just the buzzwords. Here's my writeup of what I learned through the course.

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
##### Basic structure of a Bitcoin blockchain[^2]

As you can see from the image above, the blockchain is a chain of blocks whereby each block is linked to the previous block. At a high-level, here are the core components of a Bitcoin block[^3]:

| Block Component     | Description                                               |
|---------------------|-----------------------------------------------------------|
| Size                | The size of all elements contained in the block in bytes. |
| Header              | A collection of important metadata.                       |
| Transaction Counter | Total number of transactions contained within the block.  |
| Transactions        | The list of all transactions.                             |

And here we look closer at what makes up a block header[^4]:

| Header Component    | Description                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version             | A version number that is current to the software upgrade of the network/protocol.                                        |
| Previous Block Hash | The hash pointing to the previous or parent block of the current block in the blockchain.                                |
| Merkle Root Hash    | The hash generated based on the current transactions listed in the current block.                                        |
| Timestamp           | The timestamp of when the block was created.                                                                             |
| Difficulty Target   | The difficulty level of the puzzle to be solved for this block.                                                          |
| Nonce               | Abbreviation for "Number used only once"- the number/ answer to the puzzle that the miners have to solve for this block. |


## [Basic Operations](#basic-operations)



## [What are Smart Contracts?](#smart-contracts)



## [Another Blockchain- Ethereum](#ethereum)

Fusce non velit cursus ligula mattis convallis vel at metus. Sed pharetra tellus massa, non elementum eros vulputate non. Suspendisse potenti. Quisque arcu felis, laoreet vel accumsan sit amet, fermentum at nunc. Sed massa quam, auctor in eros quis, porttitor tincidunt orci. Nulla convallis id sapien ornare viverra. Cras nec est lacinia ligula porta tincidunt. Nam a est eget ligula pellentesque posuere. Maecenas quis enim ac risus accumsan scelerisque. Aliquam vitae libero sapien. Etiam convallis, metus nec suscipit condimentum, quam massa congue velit, sit amet sollicitudin nisi tortor a lectus. Cras a arcu enim. Suspendisse hendrerit euismod est ac gravida. Donec vitae elit tristique, suscipit eros at, aliquam augue. In ac faucibus dui. Sed tempor lacus tristique elit sagittis, vitae tempor massa convallis.

## References

[^1]: [CoinMarketCap.Com](https://www.coinmarketcap.com)
[^2]: [Matthäus Wander, CC BY-SA 3.0, via Wikimedia Commons](<https://creativecommons.org/licenses/by-sa/3.0>)
[^3]: [Block Structure, via Bitcoin Wiki](https://en.bitcoin.it/wiki/Block)
[^4]: [A Decomposition Of The Bitcoin Block Header](https://www.datadriveninvestor.com/2019/11/21/a-decomposition-of-the-bitcoin-block-header/)
