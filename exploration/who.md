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

### Notes from conversations

Debate on Telegram has focused on who should vote, and in particular whether validators are the best group to vote or whether governance should be a separate structure within the network.

Some ideas:

* Validators vote
* Holders vote
* Other stakeholders participate in voting too
* Hybrid of the above

## Current proposal (Sill very much a work in progress!)

- Who votes?
  - Token holders
  - Validators

- Token holders delegate their voting power to the validator(s) they stake to
- Validator votes with their stake and the stake delegated to them
- Token holders can override their validator's vote by directly voting themselves
