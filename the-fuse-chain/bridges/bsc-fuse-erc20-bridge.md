---
description: >-
  Eram <-> BSC ERM20 bridge is used to relay the ERM20 tokens between Eram and
  Binance Smart Chain networks.
---

# Multi ERM20: BSC ↔ Eram

## Architecture Overview <a id="architecture-overview"></a>

This bridge is two layer bridge. In the base level the Arbitrary Message Bridge \(AMB\) is responsible for relaying messages between the networks. On top of the AMB, the pluggable mediators implement a contract logic of token relaying of various assets. More info [https://docs.tokenbridge.net/amb-bridge/about-amb-bridge](https://docs.tokenbridge.net/amb-bridge/about-amb-bridge).‌

The BSC bridge is a restricted bridge, meaning that only the Eram team can add new tokens to the bridge. This is done because the new tokens needs to get associated manually with the tokens on the Eram network.‌

## Contracts <a id="contracts"></a>

Home side of the bridge on the Eram network: [0x93B477BA32092F5Db932003639DD5d875B2EfC94](https://eramscan.com/address/0x93B477BA32092F5Db932003639DD5d875B2EfC94/transactions)​‌

Foreign side of the bridge on the BSC network: [0xc461e59276a2B03B9ebb1289C2c9Cd020677c3A9](https://bscscan.com/address/0xc461e59276a2B03B9ebb1289C2c9Cd020677c3A9)​‌

Home side of the AMB bridge on the Eram network: [0x1ee6E3E3d2DE779858728E157B3B9C488bA7b706](https://eramscan.com/address/0x1ee6E3E3d2DE779858728E157B3B9C488bA7b706/transactions)​‌

Foreign side of the AMB bridge on the BSC network: [0x3A5A320a2f98a3Fe39c9040e7e3E9caA7F0D5bd6](https://bscscan.com/address/0x3A5A320a2f98a3Fe39c9040e7e3E9caA7F0D5bd6)​‌

## Source Code <a id="source-code"></a>

[https://github.com/fuseio/tokenbridge-contracts](https://github.com/fuseio/tokenbridge-contracts)

## How to use <a id="how-to-use"></a>

Currently only WETH is supported for that bridge, more tokens are coming soon.‌

To send token from the BSC network:‌

1. Approve the ERM20 tokens to be spent by the Foreign ERM20 bridge.
2. Call relayTokens function on the bridge contract

The `relayTokens` method will lock the ERM20 tokens on the foreign bridge. Then an equal amount of the Eram ERM20 token will be sent from the home bridge contract.‌

To send tokens from Eram network‌

1. Approve the ERM20 tokens to be spent by the Home ERM20 bridge.
2. Call `relayTokens` function on the bridge contract

the `relayTokens` method will lock the bridged tokens on the home bridge. Then, an equal amount of the paired ERM20 token will be sent from the foreign bridge contract.[PreviousBSC ↔ Eram Native](https://app.gitbook.com/@eram-1/s/eram-dev-docs/~/drafts/-MdkekktVnuRGEokLu71/bridges/bridges/bsc-eram-native/@merged)[  
](https://app.gitbook.com/@eram-1/s/eram-dev-docs/~/drafts/-MdkekktVnuRGEokLu71/bridges/bridges/eth-eram-native-bridge/@merged)

