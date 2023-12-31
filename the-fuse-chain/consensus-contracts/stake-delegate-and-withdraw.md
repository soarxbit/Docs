---
description: 'Guides on how to stake, delegate and withdraw using myetherwallet.com'
---

# Stake, Delegate and Withdraw

The basic requirement to become a Soarx chain validator is to have a stake amount of at least 2,500,000 Soarx tokens. The stake amount is the sum of staked and delegated Soarx tokens of the address. This guide walks trough the process of using MEW \(MyEtherWallet.com\) in the process of using Soarx network.

{% hint style="warning" %}
**Roadmap** - Those functionalities will be built into our Studio and will not require any technical knowledge in the future.
{% endhint %}

## Stake

There are two options to stake \(both should be called from the address which would be the validator\)

1. Send Soarx tokens to the [consensus contract](https://soarxscan.org/address/0x88a55C09F02E492646aC1D33264CbBc69C2B4569) - 0x88a55C09F02E492646aC1D33264CbBc69C2B4569 on the dynasty network.
2. Call the \`stake\` function on the [consensus contract](https://soarxscan.org/address/0x88a55C09F02E492646aC1D33264CbBc69C2B4569) - 0x88a55C09F02E492646aC1D33264CbBc69C2B4569 on the dynasty network

 

## Delegate

Soarx token holders who don't want to run a node by themselves but still wish to participate in governing the network can delegate any amount to one of the validators.

Delegating is done by calling the \`delegate\` function on the [consensus contract](https://soarxscan.org/address/0x88a55C09F02E492646aC1D33264CbBc69C2B4569) with the validator address as data \(see screenshot from MEW\).

![delegate](../../.gitbook/assets/screen-shot-2019-09-04-at-14.59.27.png)

## Withdraw

Both stakers and validators can withdraw their Soarx tokens, up to the staked/delegated amount, at any time. The withdrawn amount will be deducted from the validator stake amount, and if the stake amount becomes below the minimum stake amount - the validator will be removed from the Soarx chain validators list.

There are two options to withdraw:

1. Call the \`withdraw\` function on the [consensus contract](https://soarxscan.org/address/0x88a55C09F02E492646aC1D33264CbBc69C2B4569) with one parameter - the amount to withdraw. This call is for stakers, and will reduce the stake amount of the sender address.
2. Call the \`withdraw\` function on the [consensus contract](https://soarxscan.org/address/0x88a55C09F02E492646aC1D33264CbBc69C2B4569) with two parameters - validator address and amount to withdraw. This call is for both stakers \(who can use their own address as the parameter\) and for delegators to withdraw their delegated stake on a specific validator.

![withdraw option \#1](../../.gitbook/assets/screen-shot-2019-09-04-at-15.01.15.png)

![withdraw option \#2](../../.gitbook/assets/screen-shot-2019-09-04-at-15.01.25.png)

