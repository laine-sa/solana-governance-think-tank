# Delegated governance authority

Validators ideally use hardware or cold wallets to manage their withdraw authorities. The withdraw authority is a master key for a vote account and as such must be protected.

To participate in on-chain governance a few options exist:

* Use the identity key (still a sensitive key that holds funds and lives as a hot wallet on the validator)
* Create a new key type `governance authority` to which governance voting authority may be delegated

This requires modifications to the VoteProgram and potentially VoteAccount structure/size. It also opens up interesting conversations around governance delegation. E.g. can multiple validators delegate their authority to the same governance authority? Could large insitutional validators such as CEXs delegate their governance authority to a service provider?

It may also be of interest to make a delegation limited in time/slots, e.g. the withdraw authority is used to authorize a governance delegation to a public key which expires after a number of slots (could be fixed or defined by the user, e.g. 100k slots). This would invariably mean each vote requires a new delegation from the withdraw authority (which would be a component of the VoteProgram similar to a commission change or withdrawal and relatively harmless, the delegate could then be a hot wallet that is used by the operator to interact with the Realms UI).
