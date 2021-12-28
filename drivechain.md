---
title: Drivechain
description: proposed Bitcoin upgrade in BIP-300 and BIP-301
published: true
date: 2021-12-28T17:25:33.789Z
tags: 
editor: markdown
dateCreated: 2021-12-26T06:03:53.200Z
---

# Drivechain

## BIP References

BIP-300, Hashrate Escrows
- https://github.com/bitcoin/bips/blob/master/bip-0300.mediawiki
- https://en.bitcoin.it/wiki/BIP_0300
- https://blog.bitnovo.com/en/bip-300-upgrade-drivechains/

BIP-301, Blind Merged Mining
- https://github.com/bitcoin/bips/blob/master/bip-0301.mediawiki
- https://en.bitcoin.it/wiki/BIP_0301
- https://bips.xyz/301

## Problem To Solve

First, let's begin with BIP-301 (Blind Merged Mining, "BMM").  Let's discuss the basics of traditional Merged Mining ("MM") to lay the groundwork for understanding BMM.



### Properties of BMM

1. per mainchain block, zero or one new sidechain block may be proposed
1. per mainchain block, zero or one sidechain fork (of potentially many) may be extended
1. per mainchain block, zero or one successfully proposed sidechain block pays fees
1. sidechain consensus only considered successfully proposed sidechain blocks
1. sidechain consensus may additionally finalize sidechain blocks
1. an attacker could propose a deep reorg fork, but the attack would be slow and visible
1. sidechain proposers would need to outbid the attacker to continue chain extension
1. until the attacker is outbid, the sidechain can't finalize more blocks
1. a sympathetic miner, of course, could be alerted to the attack to assist in extending the valid chain

### Variations

1. sidechain block proposal TXs could enforce a fee burn for unforgeable costliness (and dividend back to holders)
1. sidechain block proposal TXs should compete with all other TX types for blockspace
1. if there is no burn, total fees + MEV extracted on the sidechain would be paid to mainchain
1. if there is a burn, there is proportionally less incentive to extract fees + MEV
1. if there is a total burn, this payment nullifies the proportional incentive to extract fees + MEV
1. if there is a total burn, mainchain miners aren't incentivized to care
1. a burn can be seen as rent sought by mainchain asset holders from 


