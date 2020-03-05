---
layout: post
title: "Examining Maker Vaults (CDP) Creation Metrics From 2019"
date: 2020-3-6
image: img/Figures for Build1/maker_vault_creation_png.png
author: Mason Nystrom
---
Feel free to read the post on Medium 

MakerDAO's vaults have been the flagship product of the Decentralized Finance (DeFi) ecosystem with Maker accounting for the majority of total value locked in DeFi protocols and platforms. 

# Maker Vaults Impressive Rise to DeFi Dominance
With Maker’s impressive rise, I wanted to examine the rise of Vaults over the course of 2019 and see if there were any standout events. So, I pulled some Alethio reports as well as some Coinmetrics data about Sai(single collateral dai) and Dai(multi-collateral dai) got to work.

MakerDAO Vault users are able to perform various actions that are represented as call functions to the smart contract. Vault owners are able to perform the following:

### Create or change ownership
* Open: A user opens a new vault with a sequentially generated id.
* Give: An owner gives away ownership of a CDP to another address.

When examining the data, it appears that the Maker protocol “gives” a vault to a new user (Ethereum address) shortly after a user opens a vault. So, “give” transactions aren’t a very useful metric for gaging actual vault users. Notably, there were 260 more give transactions than opens, suggesting that 260 vaults actually transferred ownership throughout 2019.

### Adding Collateral
* Join: A user joins the collateral pool by depositing ETH in exchange for PETH. PETH is sent to the Maker contract and exchanged for DAI and PETH is locked until the DAI is repaid.
* Lock: Anytime a user adds collateral to an existing vault.

### Withdraw Collateral
* Free: Called when a user withdraws collateral from a vault.
* Exit: a user withdraws collateral (PETH) in exchange for Ether.

### Lend or repay DAI
* Draw: A user borrows DAI which is then minted and issued to the user.
* Wipe: User pays back some DAI and interest which is then burned.

### Liquidate collateral
* Bite: When a vault becomes unsafe, the collateral is liquidated and used to repay the loan until the collateralization ratio returns to a safe level.
* Shut: A vault is closed

Since opening a Maker Vault is rather trivial and users are only required to pay a small amount of gas on Ethereum, we have to further define what it qualifies as “opening” a vault. So from now on in this post “open” vaults will be counted as vaults that were both opened and joined — meaning that the user joined the Maker collateral pool by depositing Ether into their vault.

My criteria for account creation follows: a user must have opened a vault and deposited ether into the vault. In terms of Alethio’s dataset, we are looking for accounts that show both “Opened and Joined”. 
After sorting the criteria, there were 75,424 vaults opened throughout 2019, which eliminated just over 30% of all the vaults that were only opened.

### Spikes in Maker Vault Creation
As you can see from Figure 6 there were several drastic spikes of vault creation throughout the year. For instance, Maker experienced the largest and second-largest days of vault creation immediately following its announcement of Multi-Collateral Dai in October (15–16th). Over 6000 vault accounts where users opened and deposited collateral were created on October 15th alone. Also of note is the consecutive timespan of August 1st-4th which were all within the top fifteen days of most vaults created. The four days combined for a total of 9290 vaults which was 12% of the total amount of Maker Vaults created in 2019.

The likely reason for the rapid account creation in 2019 was Coinbase Earn’s “Maker Advanced Task” which required individuals to open a Maker Vault in exchange for Dai stablecoin. In fact, the Maker Advanced Task was successful that Coinbase has distributed all the Dai that was pledged to individuals who complete the lessons and Maker Vault tutorial.

This means that Coinbase Earn has certainly been the single largest decentralized finance user adoption tool/mechanism and potentially one of the most effective in crypto.

Now, one caveat is that it’s hard to determine how active those accounts were without really diving into the dataset. Tracking the long term userbase of Maker is make even more challenging with the switch to Maker’s Multicollateral Dai and the Oasis platform.

### What about the 2020 Vault Statistics and Metrics?
We could easily examine the 2020 stats for Maker single collateral vaults, however, for a few reasons it’s really not useful. First, the single collateral Dai or “Sai” has decreased rapidly over the past three months as users switch to the Multicollateral Dai. The transition to Multicollateral Dai has obviously resulted in the reduction of the Sai stablecoin (single collateral Dai) which as of March 1st sits around 21 million Sai.

Maker’s transition to multi-collateral Dai and the Dai Savings Rate (DSR) occurred on November 18th and now multi-collateral Dai’s fully diluted supply sits around 50 million Dai with a circulating supply of a little over 115 million Dai. 
As the final Sai vault users transition to multi-collateral vaults, Sai will fade away to little more than a distant memory where we’ll say to our grandkids, “I remember when we had to use only single collateral Dai”. Oh, the nostalgia. 

### Final Thoughts
Overall, 75,000 vaults opened over the course of 2019 is a historic feat for any crypto project, let alone one as complex as MakerDAO. Even if many of these accounts were opened solely because of Coinbase Earn, it’s still impressive to find such a successful marketing campaign. In a future post, I’ll revisit the number of accounts/vaults opened and compare it against 2019, as well as marketing campaigns and DeFi events to see if there are any noticeable correlations. Additional metrics to examine would be the ether held in each account in order to grasp how many users have a meaningful amount of ether in their vault. I’m very excited to watch the continued growth of Maker and other DeFi protocols in 2020.

### About the Author
I’m Mason Nystrom, a writer and aspiring angel investor. Previously I worked for ConsenSys as a marketer focused on marketing strategy for ConsenSys and its portfolio companies. Prior to joining ConsenSys, I worked as a Business Analyst at Gatecoin, the first cryptocurrency exchange to list ether, Ethereum’s native cryptocurrency.
I’m passionate about Bitcoin, Ethereum, DeFi, Web 3.0, and all things crypto. When I’m not writing or heads down in crypto, I’m learning to become a developer at Lambda School.

Advancing Web 3.0 is a weekly newsletter about cryptocurrencies, decentralized finance (DeFi), and technologies that are shaping the next era of the Internet. Welcome to the bleeding edge. Welcome to Web 3.

The views, information, and opinions expressed are solely those by the author and are meant for informational purposes only and are not intended to serve as a recommendation or investment advice to buy or sell any securities, cryptoassets, or other financial products.

