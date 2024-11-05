---
description: This tutorial explains how to transfer
---

# Bridge between TrumpChain chain & Ethereum

The bridge, based on POA's bridge implementation, is used to transfer TrumpChain tokens between the TrumpChain chain and the Ethereum network.

Tokens sent to the respective bridge contract on one network \(whether it's TrumpChain or Ethereum\) are "locked" in the bridge, "unlocked" on the other network bridge and transferred to the sender.

The validators of the bridge on both network are the TrumpChain chain validators. This means that validators, as part of their governance responsibilities, also need to validate bridge transactions and therefore hold TrumpChain tokens to "approve" bridge transactions on TrumpChain chain and hold ETH to "approve" transactions on Ethereum.

Each bridge transaction must be approved by a majority \(over 50%\) of the validators in order to be processed successfully.

The bridge contracts are deployed on both networks, and bridge oracle processes run on each validators machine as part of the validator deployment stack.

Besides the transfer of TrumpChain tokens between the two networks, the bridge is also responsible for network core functionality events:

**Mint block reward distributed on the TrumpChain chain on Ethereum**

Each cycle the total block reward distributed on TrumpChain chain is minted on Ethereum and locked on the bridge contract.

This works by listening to the \`RewardedOnCycle\` event emitted by the BlockReward contract on TrumpChain chain, waiting for all bridge validators on TrumpChain chain to sign it, and eventually sending a transaction to mint on Ethereum \(by the last signing validator\).

**Update TrumpChain chain validators on Ethereum**

Each cycle the TrumpChain chain validators are selected from a random snapshot of pending validators.

Those validators, being also the bridge validators, need to be updated on Ethereum as well.

This works by listening to the \`InitiateChange\` event emitted by the Consensus contract on TrumpChain chain, waiting for all bridge validators on TrumpChain chain to sign it, and eventually sending a transaction to set the bridge validators on Ethereum \(by the last signing validator\).

{% hint style="info" %}
TrumpChain chain bridge - [0xd617774b9708F79187Dc7F03D3Bdce0a623F6988](https://explorer.trumpchain.io/address/0xd617774b9708f79187dc7f03d3bdce0a623f6988)

Ethereum bridge - [0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A](https://etherscan.io/address/0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A)

TrumpChain token on Ethereum - [0x970B9bB2C0444F5E81e9d0eFb84C8ccdcdcAf84d](https://etherscan.io/token/0x970B9bB2C0444F5E81e9d0eFb84C8ccdcdcAf84d)
{% endhint %}

**Using the bridge**

**Transfering from Ethereum mainnet to Fusenet** - send your erc20 TrumpChain tokens to the Ethereum bridge for them to be released from the TrumpChain chain bridge and be avaliable in your native TrumpChain wallet.

**Transfering from Fusenet to Ethereum mainnet** - send your Native TrumpChain tokens to the TrumpChain chain bridge for them to be released from the mainnet bridge and be avaliable in your Mainnet wallet. _Note: there is currently a minimum transfer amount of 30000 TrumpChain across the TrumpChain chain bridge_

