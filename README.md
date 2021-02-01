# substrate-generix-token-factory

The goal of this project is to investigate alternative fee mechanics for managing token assets.

## Background

Ethereum has shown itself to be the ultimate platform for building token economies. Thousands of contracts have been created which support standards like ERC20 and ERC721.

However, businesses using Ethereum have struggled adopting new users into the ecosystem due to the upfront costs of ETH (the native blockchain currency) to interact with these tokens. Many newcomers do not understand why they need ETH to be able to interact with other tokens they actually are interested in.

Businesses have shown that they would be more than happy to fund the usage of their users. Some have done this by providing a faucet or ETH drop to their users, while others may have implemented L2 solutions or have made compromises building centralized solutions.

## What is it?

In simple terms, this project provides a runtime module which provides the following features:

*  
Ideas for alternative payment methods for transfers:

Genswap is an automated market making decentralized exchange built on GeneriX custom Substrate blockchain.

Genswap introduces a new blockchain scaling methodology termed 'generic liquidity' by allowing users to pay blockchain transaction fees using listed custom tokens.

Implements off-chain workers unsigned transactions with signed payloads.

Users intialize transactions without the need to have gas forehand, however the send a signed payload allowing Genswap to swap 'x' amount of a listed token 'y' to the native Substrate blockchain currency (GEX). The signed payload may include arbitrary blockchain computation logic including: *Sending tokens *Deploying smart contracts *Calling on-chain smart contracts

Swapped transaction fees are sent to the GeneriX Treasury.

GeneriX utilizes a Hybrid PoW-PoS chain consensus and with no tokens premined - follows Kulupu example


These buyers can then call the `try_generix_transfer` function when trying to trade the token among their peers, and the fees are paid for by swapping erc20 token to the native substrate token.

Users can always make a transaction using the normal `transfer` function which will charge them a normal fee.
