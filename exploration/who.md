---
description: The stakeholders
---

# Who

## Introduction

There are numerous stakeholders to an L1 governance process. These include the teams building the clients, the operators (validators & RPC operators), the token-holders (delegators), as well as all the other projects and teams building on the L1 who may be impacted by governance decisions.

It is important to create a forum that allows all stakeholders to be heard and to participate actively, fairly and constructively.

At the same time it is important to determine clearly how decisions are made. Solana uses a delegated proof of stake protocol, whereby token-holders delegate the power of their tokens to validators, who use this power to vote on the validity of blocks of transactions.

It seems natural that if validators may choose which blocks and thus which transactions are valid (and currently one validator at a time also chooses which transactions even go into blocks), that this same delegated voting power is used for governance.

It is however likely still desirable to permit other stakeholders (i.e. anyone) to create governance proposals (with disincentives for abuse), to participate in debate around proposals and to lobby for a particular outcome.

## Key Questions to Answer

### Who votes?

Which stakeholders within the Solana community vote?

- Client building teams
- Infrastructure (validator and RPC) operators
- Tokenholders
- Dapp developers
- Other (TBD)

A related question is whether voting requires ownership of SOL. If it does, this requirement by default may define the stakeholder set, e.g. to token holders and validators, if token holders delegate their voting power to validators. If it doesn't, the stakeholder set can be more widely defined, making the question listed below regarding how voting power is assigned all the more important.

Do all stakeholders vote on all governance topics defined in the "What" section?

### How is voting power allocated?

What mechanism is used to assign voting power to the various stakeholders defined above?

- Stake-weighted voting power allocation, e.g. 1 token = 1 vote
- Quadratic voting
- Other (TBD)

## Current Proposals

Note that as of August 10, 2023, conversations seem to be favoring option 1 so far.

### Proposal A - Validators Only

#### Description

Validators are the only stakeholders who vote. Validator votes are stake-weighted.

Those supporting this proposal suggest that stake account holders can express their desired vote outcome by either staying staked to their validator if they agree with their selected validator's voting or delegate away from their selected validator if they disagree with the way that validator votes.

There is currently a difference of opinion as to whether there should be a time window within the governance timeline for stake account holders to make this decision or whether the current unstake functionality is sufficient. Detractors have expressed an opinion this is a less inclusive approach than Proposals 2 or 3.

### Proposal B - Validators and Stake Accounts

#### Description

Validators and stake account owners vote. Validator and stake account votes are stake-weighted. Validator votes on behalf of stake account holders. Stake account holders can override the vote of their validator.

This option is similar to how voting works on Cosmos. Those supporting this proposal feel that it is a more inclusive approach than Proposal 1. Detractors question the technical feasibility of allowing such a large number of stake accounts (~500k) to vote, as well as the value the stake holders will provide through their votes.

### Proposal C - Validators, Stake Accounts and Other Stakeholders

Validators, stake account holders and other stakeholders, such as RPC operators and Dapp developers vote. Voting power is not distributed via stake weight.

This proposal is under development [here](https://hackmd.io/RyGbl7RLQAmDHAZG-6gfMA?utm_source=comment-card&utm_medium=icon).

## Notes from conversations

Debate on Telegram has focused on who should vote, and in particular whether validators are the best group to vote or whether governance should be a separate structure within the network.

Some ideas:

* Validators vote
* Holders vote
* Other stakeholders participate in voting too
* Hybrid of the above
