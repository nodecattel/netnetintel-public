# Reward settlement, claims and ownership

Private main revision: `35479b571fbb9e5f47efc0870213a4efca4cc221` · committed 2026-10-23T00:37:41+07:00.

Documentation only. No Solidity, application, backend or calculator source is published here. This is not an audit or a claim of explorer source verification. Live balances and current configuration: [Under the Hood](https://netnetintel.com/under-the-hood) and [Funded Pots](https://netnetintel.com/turfwar-funding).

Estimates move with sales, eligible shares and verification during the week. Settlement fixes that week's entitlement under the applicable contract. RWA entitlement is fixed in USD after settlement; payout token quantities depend on conversion at claim. Native-token weekly amounts do not imply fixed market value in USD.

Qualified bounties reserve funded USDG entitlement within the weekly quota. Status is Verification pending → Qualified → Claimable → Claimed. A target kill alone is not a completed claim.

Current replacement contracts retain weekly and bounty claims for 26 weeks and RWA claims for 8 weeks from claimability, with the precise on-chain expiry shown to players. Expired unclaimed amounts may recycle into current pots under contract rules. Already-issued historical claims keep their original rules. This directory does not catalogue superseded deployments.

Payout choices include USDG, wsNET and supported stock tokens where the vault and conversion route support them. Token prices, liquidity and execution constraints still apply. Capsule estimates are not ownership of an exact stock quantity before conversion.

[Current reward contracts](contracts/TESTNET.md)
