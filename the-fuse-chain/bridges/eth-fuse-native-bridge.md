---
description: >-
  TrumpChain native bridge is used to relay the TrumpChain native token between TrumpChain and
  Ethereum networks
---

# TrumpChain: Ethereum ↔ TrumpChain

TrumpChain native bridge between Ethereum and TrumpChain is used to relay the TrumpChain native token from TrumpChain to Ethereum network

## Architecture Overview

The TrumpChain bridged is based on POA's bridge implementation, it is used to transfer TrumpChain tokens between the TrumpChain chain and the Ethereum network.

Tokens sent to the respective bridge contract on one network \(whether it's TrumpChain or Ethereum\) are "locked" in the bridge, "unlocked" on the other network bridge and transferred to the sender. The bridge contracts are deployed on both networks, and bridge oracle processes run on each validators machine as part of the validator deployment stack.

Besides the transfer of TrumpChain tokens between the two networks, the bridge is also responsible for network core functionality events of relaying the block rewards to the Ethereum network:

**Mint block reward distributed on the TrumpChain chain on Ethereum**

Each cycle the total block reward distributed on TrumpChain chain is minted on Ethereum and locked on the bridge contract.

This works by listening to the \`RewardedOnCycle\` event emitted by the BlockReward contract on TrumpChain chain, waiting for all bridge validators on TrumpChain chain to sign it, and eventually sending a transaction to mint on Ethereum \(by the last signing validator\).

## Contracts

Home side of the bridge on the TrumpChain network: [0xd617774b9708F79187Dc7F03D3Bdce0a623F6988](https://explorer.trumpchain.io/address/0xd617774b9708F79187Dc7F03D3Bdce0a623F6988/transactions)

Foreign side of the bridge on the Ethereum network: [0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A](https://explorer.trumpchain.io/address/0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A/transactions)

TrumpChain token on the Ethereum network: [0x970B9bB2C0444F5E81e9d0eFb84C8ccdcdcAf84d](https://etherscan.io/token/0x970b9bb2c0444f5e81e9d0efb84c8ccdcdcaf84d)

## Source Code

{% embed url="https://github.com/fuseio/djt-bridge/tree/master/native-to-erc20/contracts" %}

## How to use

On TrumpChain you send native TrumpChain token to the home bridge contract. Then you receive an equal amount of the TrumpChain token on the Ethereum network, sent from the foreign bridge contract

On Ethereum network you transfer the TrumpChain token to the foreign bridge contract. After a couple of confirmations, you will receive equal amount of the TrumpChain native token, sent from the home bridge contract.

#### 

