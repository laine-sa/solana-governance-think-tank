# Vote locking & redelegation

Another learning from Cosmos is that token-holders may override the vote of their delegate validator.

This means that a validator might hold 1% of stake-weight, but one of their delegators who themselves has delegates 0.1% of stake-weight to this validator could choose to vote differently, thus reducing the validator's vote by 0.1% to 0.9% and adding their 0.1% to a different voting option.

While this is an intrigueing concept it also carries some problems with it: it requires constant attention and understanding of delegators, while not penalizing validators for voting against the wishes of their delegators.

A proposed alternative option for Solana, supported by the `Redelegate` instruction that will soon become available on Mainnet-Beta:

* Once a proposal opens for voting, validators have a fixed time period to vote, e.g. 7 days
* During the voting period validators may cast a vote and may amend their already cast vote to a different option
* After the voting period ends the validators' votes are locked and a redelgation period exists for another time period, e.g. 3 days
* During this period delegators may redelegate their stake, e.g. from a No-voting validator to a Yes-voting one, thereby altering the outcome of the final tally

This method incentivises validators to vote wisely and listen to the opinions and wishes of their delegators, while penalizing those who don't. It further encourages good staking choices by delegators who are empowered to support validators who are active in governance and vote well&#x20;

{% hint style="info" %}
This method can also incentivise a redelegation from a non-participating validator to a participating one, not purely based on the substance of the vote but simply the participation in governance as a signal of goodness.
{% endhint %}
