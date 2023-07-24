---
description: Why does Solana need structured on-chain governance
---

# Why



## Status quo

Governance on Solana currently does exist in a very "soft" form.&#x20;

Currently (July 2023) only a single validator client exists on Solana ("Labs client"). While a fork in the form of jito-solana exists this is not a standalone client is broadly the same implementation.&#x20;

This allows for a high-velocity development environment, which until now has been needed. However as Solana matures and further clients are developed we require a more methodical and planned approach.

With a single client the core contributors of the Labs client can effectively decide on alterations to the protocol, runtime and many underlying tuning parameters. This either happens through a direct change which doesn't break consensus, or via a feature gate, which requires an on-chain activation. A feature gate triggers a hard fork where incompatible older nodes are unable to continue validating the global state.&#x20;

Feature gates are activated via the feature program on-chain, with a private key unique to each feature gate which is owned by the core contributor associated to that feature gate. Activation is managed via a schedule and social consensus.

### Current on-chain voting

A current implementatin of on-chain stake-weighted voting by validators does exist. This is a component of the feature program.

However it has several drawbacks:

* Validators receive an airdrop of tokens to vote with, the distribution of these tokens is manual and could be manipulated
* Validators must use a CLI tool to cast a YES vote
* No other vote is possible
* This leads to a natural pressure as the only score one can track and lobbied for is "YES" votes, while it also takes away the ability to actively dissent with a change, absence of a YES vote may be an abstention or a NO vote or no vote at all, indicating lack of engagement.
* There is no UI, thus while validators are technically capable it is opaque to other users and given the ambiguity between no, abstain and ignorance presents further confusion in interpretating non-votes.
* Difficult to maintain a record of past voting by validators (and would only indicate YES or non-participation)



## Resilience and Independence

As Solana matures, we seek growing independence from any single entity or actor, as well as resilience to their potential mealfeasance.

Combined with a strong and broad stake distribution as well as very active set of validators the time is suitable to seek a transition to stronger on-chain governance.&#x20;

One example of how some groups in the community began this conversation previously is the proposal to increase the minimum stake delegation from 1 lamport to 1 SOL. This is an example of a type of change that should go through a full governance voting process, with a defined central location for debate and subsequent permanent voting record with the ability to dissent or abstain.
