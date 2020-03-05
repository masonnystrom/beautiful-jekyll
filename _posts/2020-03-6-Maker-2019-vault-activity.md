---
layout: post
title: "Examining Maker Vaults (CDP) Creation Metrics From 2019"
date: 2020-3-6
image: maker_vault_creation.png
author: Mason Nystrom
---

MakerDAO's vaults have been the flagship product of the Decentralized Finance (DeFi) ecosystem with Maker accounting for the majority of total value locked in DeFi protocols and platforms. 

## Maker Vaults Impressive Rise to DeFi Dominance

With Maker's impressive rise, I wanted to examine the rise of Vaults over the course of 2019 and see if there were any standout events. So, I pulled some Alethio reports as well as some Coinmetrics data about Sai(single collateral dai) and Dai(multi-collateral dai) got to work.

MakerDAO Vault users are able to perform various actions that are represented as call functions to the smart contract. Vault owners are able to perform the following:

### Create or change ownership
Open: A user opens a new vault with a sequentially generated id.
Give: An owner gives away ownership of a CDP to another address.
