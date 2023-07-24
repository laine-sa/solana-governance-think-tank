# How

There appear to exist requirements for at least two components

* forum for discussion & debate
* UI for creation of proposals and voting

A [forum currently exists](https://forum.solana.com/) (recently revived). This seems like a suitable venue to create governance discussions for current and future proposals.

For the actual proposal and voting an existing on-chain program built by Solana Labs exists: spl-governance. A user-friendly UI for this exists on [Realms](https://realms.today/) - all this code is open-source and published on the Solana Labs github account.

To enable seamless stake-weighted voting two components would be required:

* on-chain view of epoch stakes (efforts are [underway ](https://github.com/solana-foundation/solana-improvement-documents/pull/56)to enable this) and an integration/plugin to Realms to assign DAO weights on this basis
* delegation of governance authority from a vote account withdraw authority to a new public key (to ensure validators do not need to use their withdraw authority to interact with the governance UI)

The actual lifecycle of a proposal and voting procedure is the area where a lot of customisation and flexibility exist, and where we can harness the learnings from other chains who have experience with governance, e.g. Cosmos. Some of these are touched on in the Practicalities section.
