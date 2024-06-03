---
description: This tutorial explains how to transfer
---

# Bridge between Eram chain & Ethereum

The bridge, based on POA's bridge implementation, is used to transfer Eram tokens between the Eram chain and the Ethereum network.

Tokens sent to the respective bridge contract on one network \(whether it's Eram or Ethereum\) are "locked" in the bridge, "unlocked" on the other network bridge and transferred to the sender.

The validators of the bridge on both network are the Eram chain validators. This means that validators, as part of their governance responsibilities, also need to validate bridge transactions and therefore hold Eram tokens to "approve" bridge transactions on Eram chain and hold ETH to "approve" transactions on Ethereum.

Each bridge transaction must be approved by a majority \(over 50%\) of the validators in order to be processed successfully.

The bridge contracts are deployed on both networks, and bridge oracle processes run on each validators machine as part of the validator deployment stack.

Besides the transfer of Eram tokens between the two networks, the bridge is also responsible for network core functionality events:

**Mint block reward distributed on the Eram chain on Ethereum**

Each cycle the total block reward distributed on Eram chain is minted on Ethereum and locked on the bridge contract.

This works by listening to the \`RewardedOnCycle\` event emitted by the BlockReward contract on Eram chain, waiting for all bridge validators on Eram chain to sign it, and eventually sending a transaction to mint on Ethereum \(by the last signing validator\).

**Update Eram chain validators on Ethereum**

Each cycle the Eram chain validators are selected from a random snapshot of pending validators.

Those validators, being also the bridge validators, need to be updated on Ethereum as well.

This works by listening to the \`InitiateChange\` event emitted by the Consensus contract on Eram chain, waiting for all bridge validators on Eram chain to sign it, and eventually sending a transaction to set the bridge validators on Ethereum \(by the last signing validator\).

{% hint style="info" %}
Eram chain bridge - [0xd617774b9708F79187Dc7F03D3Bdce0a623F6988](https://eramscan.com/address/0xd617774b9708f79187dc7f03d3bdce0a623f6988)

Ethereum bridge - [0x476c29c5589BFE3C0E4A509bb92545882bb4Db82](https://etherscan.io/address/0x476c29c5589BFE3C0E4A509bb92545882bb4Db82)

Eram token on Ethereum - [0x970B9bB2C0444F5E81e9d0eFb84C8ccdcdcAf84d](https://etherscan.io/token/0x970B9bB2C0444F5E81e9d0eFb84C8ccdcdcAf84d)
{% endhint %}

**Using the bridge**

**Transfering from Ethereum mainnet to Fusenet** - send your erc20 Eram tokens to the Ethereum bridge for them to be released from the Eram chain bridge and be avaliable in your native Eram wallet.

**Transfering from Fusenet to Ethereum mainnet** - send your Native Eram tokens to the Eram chain bridge for them to be released from the mainnet bridge and be avaliable in your Mainnet wallet. _Note: there is currently a minimum transfer amount of 30000 Eram across the Eram chain bridge_

