---
description: Becoming a Eram validator in a few simple steps
---

# Getting started as a validator

## Pre-requirements

In order to be a Eram validator, you first must see that you meet the pre-requirements:

* You know what it means to be a Eram validator - [Becoming a validator](how-to-become-a-validator.md#what-it-means-to-be-a-validator).
* You have at least 200 ERAM tokens or you will have an aggregated delegation of at least 200 ERAM tokens \(you can purchase ERAM token on [Uniswap](https://uniswap.exchange/swap/0x970b9bb2c0444f5e81e9d0efb84c8ccdcdcaf84d)\).
* You have an always-on hardware that meets the pre-requisites - [Running a validator node](run-your-own-validator.md#pre-requisites)

## How to become a Eram validator

## Run Local Node

Read more at: [https://github.com/eramsmartchain/CoinNetwork/tree/master/node-example](https://github.com/eramsmartchain/CoinNetwork/tree/master/node-example)

#### Delegate

To delegate, just send the ERAM tokens from any address to the Consensus contract address with the data: `0x5c19a95c000000000000000000000000<address without 0x>`.

{% hint style="success" %}
Example:

For the address: `0xb8ce4a040e8aa33bbe2de62e92851b7d7afd52de`  
Use: `0x5c19a95c000000000000000000000000b8ce4a040e8aa33bbe2de62e92851b7d7afd52de` as the data.

`5c19a95c` is for the `delegate(address)` function signature.

`b8ce4a040e8aa33bbe2de62e92851b7d7afd52de`in this example is an address you're delegating to \(without the `0x` prefix\)
{% endhint %}

### Step 6: Wait for 1 cycle \(approximately 48 hours\).

Wait until the next cycle is started.

{% hint style="success" %}
You can see that you are validating both in the [health](https://status.eramscan.com/) site and on the [explorer](https://eramscan.com) site.
{% endhint %}

For live support, contact us on [Telegram](https://t.me/) or [Discord](https://discord.gg/). Good luck and happy validating!

