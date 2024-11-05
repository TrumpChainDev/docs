---
description: 'Guides on how to stake, delegate and withdraw using myetherwallet.com'
---

# Stake, Delegate and Withdraw

The basic requirement to become a TrumpChain chain validator is to have a stake amount of at least 200 TrumpChain tokens. The stake amount is the sum of staked and delegated TrumpChain tokens of the address. This guide walks trough the process of using MEW \(MyEtherWallet.com\) in the process of using TrumpChain network.

{% hint style="warning" %}
**Roadmap** - Those functionalities will be built into our Studio and will not require any technical knowledge in the future.
{% endhint %}

## Stake

There are two options to stake \(both should be called from the address which would be the validator\)

1. Send TrumpChain tokens to the [consensus contract](https://explorer.trumpchain.io/address/0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A) - 0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A on the djt network.
2. Call the \`stake\` function on the [consensus contract](https://explorer.trumpchain.io/address/0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A) - 0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A on the djt network

 

## Delegate

TrumpChain token holders who don't want to run a node by themselves but still wish to participate in governing the network can delegate any amount to one of the validators.

Delegating is done by calling the \`delegate\` function on the [consensus contract](https://explorer.trumpchain.io/address/0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A) with the validator address as data \(see screenshot from MEW\).

![delegate](../../.gitbook/assets/screen-shot-2019-09-04-at-14.59.27.png)

## Withdraw

Both stakers and validators can withdraw their TrumpChain tokens, up to the staked/delegated amount, at any time. The withdrawn amount will be deducted from the validator stake amount, and if the stake amount becomes below the minimum stake amount - the validator will be removed from the TrumpChain chain validators list.

There are two options to withdraw:

1. Call the \`withdraw\` function on the [consensus contract](https://explorer.trumpchain.io/address/0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A) with one parameter - the amount to withdraw. This call is for stakers, and will reduce the stake amount of the sender address.
2. Call the \`withdraw\` function on the [consensus contract](https://explorer.trumpchain.io/address/0x3FA18721a6D5eAd62d77f1E9DA4D848d4fb4461A) with two parameters - validator address and amount to withdraw. This call is for both stakers \(who can use their own address as the parameter\) and for delegators to withdraw their delegated stake on a specific validator.

![withdraw option \#1](../../.gitbook/assets/screen-shot-2019-09-04-at-15.01.15.png)

![withdraw option \#2](../../.gitbook/assets/screen-shot-2019-09-04-at-15.01.25.png)

