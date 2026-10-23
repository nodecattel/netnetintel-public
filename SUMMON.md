# Summon mechanics and proof boundaries

Private main revision: `3ac1c58fd0031891b2c551719332cde75ee29a52` · committed 2026-10-23T07:11:28+07:00.

Documentation only. No Solidity, application, backend or calculator source is published here. This is not an audit or a claim of explorer source verification. Live balances and current configuration: [Under the Hood](https://netnetintel.com/under-the-hood) and [Funded Pots](https://netnetintel.com/turfwar-funding).

A wallet submits an accepted ticket, then commit/reveal settlement fixes its outcome. Keys are burned at settlement. Unsettled paid tickets have a 24-hour reclaim path under the desk rules. Confirm transaction state before resubmitting.

| Tier | Probability |
| --- | --- |
| D | 45% |
| C | 25% |
| B | 15% |
| A | 10% |
| S | 4% |
| S+ | 1% |

The proof binds the ticket, commitment/reveal and deterministic tier result. Simulation and replay verification subsequently determine run details and eligible capsule rewards. Show confirmed base outcomes early; capsule rewards remain Verifying until that step finishes. Batch results retain every accepted ticket and its state.

This is not a claim of Chainlink VRF or drand randomness. Commit/reveal integrity, operator/keeper availability, backend simulation correctness and settlement publication are distinct trust boundaries. A transaction being mined does not by itself prove the full run simulation.

[Current SummonDesk](contracts/TESTNET.md) · [Reward formulas](CALCULATIONS.md)
