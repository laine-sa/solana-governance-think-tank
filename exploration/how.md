# How

## Components

There appear to exist requirements for at a number components -

* Forum for discussion & debate
* UI for creation of proposals and voting
* Mechanism for voting result execution

### Discussion Forum

A [forum currently exists](https://forum.solana.com/c/gov/11) (recently revived). This seems like a suitable venue to create governance discussions for current and future proposals.

### UI for proposal creation and voting

For the actual proposal and voting an existing on-chain program built by Solana Labs exists: spl-governance. A user-friendly UI for this exists on [Realms](https://realms.today/) - all this code is open-source and published on the Solana Labs github account.

To enable seamless stake-weighted voting two components would be required:

* on-chain view of epoch stakes (efforts are [underway ](https://github.com/solana-foundation/solana-improvement-documents/pull/56)to enable this) and an integration/plugin to Realms to assign DAO weights on this basis
  
* delegation of governance authority from a vote account withdraw authority to a new public key (to ensure validators do not need to use their withdraw authority to interact with the governance UI)

### Voting result mechanism execution

Once a vote is taken and the results compiled, it is necessary for an action to be taken, probably on-chain, to reflect the vote result. A mechanism is required to execute this action.

## Lifecycle and timeline

The actual lifecycle of a proposal and voting procedure is the area where a lot of customisation and flexibility exist, and where we can harness the learnings from other chains who have experience with governance, e.g. Cosmos. Some of these are touched on in the Practicalities section.

* Proposal submitted
* Discussion period
* Quorum reached or not
* Vote
* Vote result execution

## Foundation Perspective - Added October 23, 2023

From Dan Albert, source link [here](https://discord.com/channels/1030192322769596496/1137345959949512734/1166032931706380359).

Hi all, really appreciating seeing the community start to ramp up more thoughtful discussion around governance.  I want to share a few more tactical updates that you all might be interested in.

1)  SIMD-72 [1] proposes an automated activation process for new feature gates.  This would distribute the activation process out to the validators and their respective software versions, rather than the current method which activates based on a single signer.  This was the topic of the most recent Core Dev call last week [2]

2)  Starting with the 1.17 release from Solana Labs, before this or any future branch would be proposed for Mainnet adoption, all new feature gates will be mapped to a corresponding SIMD in the release notes or similar update doc.

3)  Solana Foundation is hiring for a Technical Program Manager (TPM) to act as a full time liaison/coordinator for the core protocol development process [3].  The goal here is to act as a better steward of the SIMD process and all the human coordination that takes place before (research, experiments, initial proposals), during (formal SIMD proposal, debate, social consensus, some level of governance), and after (implementation in the multiple validator codebases, integration testing, adoption and activation on Mainnet).  The process is still immature and rather high friction for a lot of people, and Foundation desires to act as a coordinating (not dictating) entity so that anyone in the community can discover, navigate and participate in the process of steering the Solana protocol.

[1] https://github.com/solana-foundation/solana-improvement-documents/pull/72

[2] https://twitter.com/i/broadcasts/1YqKDgWjakNxV

[3] https://jobs.ashbyhq.com/Solana%20Foundation/af17443d-406d-419b-9116-1e4db2bc4468?utm_source=Solana+Network+Opportunities+job+board&utm_medium=getro.com&gh_src=Solana+Network+Opportunities+job+board

## Interim Process - Introduction

As of September 18, 2023

The discussion over the past two months has resulted in three Why proposals and two What proposals. It's now time to start moving toward making initial decisions. 

To make these iniial decisions requires an interim process. This interim process with follow the logic of a "minimum viable process". It's purpose is to facilitate these initial decisions. It is expected that this interim process will evolve as discussion moves from the WHo and Why to How. Because of this, it's important that the interim process serves the purpose it's intended to serve, without it getting stuck in a loop of over-engineering.

The curent proposal, discussed in a recent [community-led validator call](https://hackmd.io/1DFauFMWTZG37-U7CXhxMg?view#Meeting-Notes-Summary), suggests using the existing feature of governance that exists on chain. It's current implementation includes stakeweighted voting and was orginally intended to activate features.

What's needed is a CLI tool to create a feature proposal. A token and distribution schedule will be created for all the validators. The only voting option available through this process will be a "yes". A possible workaround is to send tokens to one address to indicate a "yes" vote and another address to indicate a "no" vote. The logic to do this in the case of choosing one out of three choices, as required by the "Who" vote, is to be determined.

## Interim Process - Timeline

### Step 1 - Proposal submission

* Duration - 1 day
  
### Step 2 - Initial discussion period

* Duration - 2 weeks
* Date - TBD
* Venue
  * Solana Discussion Forum post

### Step 3 - Voting period

* Duration - 1 week
* Start / End dates - TBD / TBD
* Venue
  * CLI tool to place votes
  * Solana Discussion Forum posts to communicate individual votes and reasoning behind them
 
Note that a TBD quorum must be reached for the vote to be considered valid.

#### Proposed voting process

Tokens for each vote will be created and sent to each validator's identity account. There is an existing SPL CLI for this as part of the feature proposal process. This can be used even if no feature actually exists in the costs.

It will cost 4-5 SOL per vote to create and distribute tokens into token accounts for all validators.

The current process only has a single "YES" vote option, this will be modified by providing addresses for each option. Balnces will need to be manually monitored. Full detail on how to verify all balances and amounts will be shared. The CLI automatically creates a stake-weighted distribution CSV.

https://spl.solana.com/feature-proposal

The first "informative" vote will be:

Who should cast votes in a future governance process?
-- Only validators, weighted by stake
-- Validators and Delegators, if a delegator votes it overrides that portion of the validator's stake-weight
-- Validators & other stake-holders

See proposal details [here](https://sg.laine.one/exploration/who#current-proposals).

### Step 4 - Vote result publication

* Duration - 1 day
* Date - TBD
* Venue
  * Solana Discussion Forum post communicating vote result and back-up informatino

### Next steps, i.e. implementation

It is expected that these vote will be adhered to when the more form governance process is defined and adopted. Until then, they will be used as the foundation from which to begin developing the more formalized and longer-term How process.
 
    

 
