---
title: Tokens on Canto
description: token supply, distribution, inflation, issuance, bridging
published: true
date: 2022-08-17T21:04:26.329Z
tags: 
editor: markdown
dateCreated: 2022-08-17T18:19:29.001Z
---




# Token Distribution

Canto has a native token, CANTO, which is used to pay fees and can be staked to secure the network.

## Total Supply

via [the launch announcement on Mirror](https://mirror.xyz/0x4CeD9817cAD891aEFfbF5Fb7DcB6f3c6aEBd4228/6UtxzGXsyCt6onAZjqwinAlQXhmq41Ow9o5SvPRkNKo):

>At genesis, 1B tokens were minted. The tokens will be distributed in the following manner:
> - Contributors: 13.0%
> - Settlers of Canto: 2%
> - Future Grants: 5%
> - Medium-Term Liquidity Mining: 35%
> - Long-Term Liquidity Mining: 45%
>
> Tokens not yet distributed (Grants and Future Liquidity Mining) will be kept in the 
> community pool.

Medium-Term liquidity incentives will be distributed over the first six months after launch; Long-Term incentives will be distributed over some number of years (10?).

## Airdrop

If you didn't get the airdrop and think you should have, fill out the form in [the #airdrop-form Discord channel](https://discord.com/channels/993968517906960445/1009274306133508147) and wait (patiently!) for a response: https://forms.gle/LR16PdAPF6ox1csy8


# Bridging
## Ethereum to Canto

The canonical bridge for Canto is the Gravity Bridge Chain, an independent, sovereign Cosmos zone that operates a bridge between Cosmos chains and Ethereum.

- use the GBC bridge: https://bridge.canto.io/
- read more about GBC: https://www.gravitybridge.net/
- GBC bridge UI run by Blockscape: https://bridge.blockscape.network/ (UNTESTED)

The GBC bridge deposit contract on Ethereum is [0xa4108aa1ec4967f8b52220a4f7e94a8201f2d906](https://etherscan.io/address/0xa4108aa1ec4967f8b52220a4f7e94a8201f2d906).

## Cosmos Zones to Canto

Canto also supports assets from other Cosmos chains; these assets can be bridged to Canto using the native Cosmos IBC bridge.

> Assets bridged to Canto by IBC can only be used in Canto EVM applications by converting them into Canto ERC-20 tokens.  Canto governance controls the list of supported tokens that can be converted.  For example, see [governance proposal #4 to map Canto ERC-20 tokens for Cosmos Hub's ATOM token](https://governance.canto.io/).
{.is-info}

Canto IBC assets:

| Token | Source | Destination | ERC-20 |
|---|---|---|---|
| ATOM | [Cosmos Hub channel-358](https://www.mintscan.io/cosmos/relayers/channel-358) | Canto channel-2 |  [0xecEEEfCEE421D8062EF8d6b4D814efe4dc898265](https://evm.explorer.canto.io/token/0xecEEEfCEE421D8062EF8d6b4D814efe4dc898265/) |
| gbcETH  | [GBC channel-88](https://www.mintscan.io/gravity-bridge/relayers/channel-88) | Canto channel-0 |  [0x5FD55A1B9FC24967C4dB09C513C3BA0DFa7FF687](https://evm.explorer.canto.io/token/0x5FD55A1B9FC24967C4dB09C513C3BA0DFa7FF687/) |
| gbcUSDC | [GBC channel-88](https://www.mintscan.io/gravity-bridge/relayers/channel-88) | Canto channel-0 | [0x80b5a32E4F032B2a058b4F29EC95EEfEEB87aDcd](https://evm.explorer.canto.io/token/0x80b5a32E4F032B2a058b4F29EC95EEfEEB87aDcd/) |
| gbcUSDT | [GBC channel-88](https://www.mintscan.io/gravity-bridge/relayers/channel-88) | Canto channel-0 | [0xd567B3d7B8FE3C79a1AD8dA978812cfC4Fa05e75](https://evm.explorer.canto.io/token/0xd567B3d7B8FE3C79a1AD8dA978812cfC4Fa05e75/)  |
| 1 | 2 | 3 | 4 |


