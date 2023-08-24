---
description: What does governance mean and entail
---

# What

An initial, incomplete list of types of governance decisions that may exist in an L1 environment such as Solana:

* Technology
  * Protocol-altering technical changes
    * Major
    * Minor
  * Parameter updates
  * Changes to consensus thresholds (ideally these are on-chain parameters), such as supermajority definition, fork switch threshold etc
  * Upgrade timelines and approvals
  * Client adoption
  * Feature activation
  * [SIMD](https://www.soldev.app/simd) Implementation approval (SIMD published, initial debate finalized, vote on whether to implement) (Possibly move to the "How" section?)
* Economics
  * Inflation and staking rewards changes
  * Transaction fees (especially once transaction fees have been overhauled and hopefully include on-chain parameters)
  * Minimum commission
* Governance
  * Adoption of the iniial governance process
  * Changes to governance itself
* Treasury management
  * Grants (if funding exists)
  * Community fund spending (if funding exists)
* Social
  * Votes on censure of validator behavior
  * Terminology/naming of things

Initially minor protocol-altering technical changes should likely not fall under governance, e.g. altering the account of a native program or a SYSVAR to accommodate more data as part of a performance or feature enhancement.

Major protocol changes as well as economic changes should likely fall under governance.

Whether a community fund should or will exist is a further debate. The Solana Foundation administers an ecosystem fund, and there is a case to be made that some portion of this should potentially be made available for administration through governance, e.g. for grants or other development that the community wishes to decide on, independent of the Foundation.

## Current Proposal(s)

The following are the leading Phase 1 implementation proposals that have emerged from discussions so far. The goal is to define a scope that is both practically limited and technically achievable, as Phase 1 is intended to the the first implementation phase of this newly defined governance process.

### Proposal A

In scope are proposed changes to - 

* Economics (parameters taken from [Solana Docs](https://docs.solana.com/inflation/terminology))
  * Total current supply (SOL)
  * Inflation rate (%)
  * Inflation schedule
  * Effective inflation rate (%)
  * Staking yield (%)
  * Total dilution (%)
  * Adjusted staking yield (%)
  * Slashing (not currently defined in Solana docs)
 
   Additional reference [Basic economic design](https://docs.solana.com/transaction_fees#basic-economic-design).

* Consensus (reference [Shinobi Systems PoS and PoH Primer](https://www.shinobi-systems.com/primer.html))
  * 67% of stake weight required for consensus
  * Leader schedule
    * Selection
    * Enforcement
  * Proof of history
    * Clock specification
    * Block streaming process

### Proposal B

In scope are proposed changes to - 

* Native programs list taken from [Solana Docs](https://docs.solana.com/developing/runtime-facilities/programs)
  * System program
  * Config program
  * Stake program
  * Vote program
  * BPF loader
  * Ed25519 program
  * Secp256k1 program

* Major feature developments/proposals
  * Generally intended to be consistent with the emerging [SIMD process](https://github.com/solana-foundation/solana-improvement-documents/blob/main/proposals/0001-simd-process.md)
  * "Major" is TBD, examples given from the existing process, linked in the previous bullet point
    * Include
      *  A change in format of a RPC API method
      * Networking interface changes between validators
      * Compute requirement changes on the runtime
    * Exclude
      * Rephrasing, reorganizing, refactoring, or otherwise "changing shape does not change meaning".
      * Additions that strictly improve objective, numerical quality criteria (warning removal, speedup, better platform coverage, more parallelism, trap more errors, etc.)
   
