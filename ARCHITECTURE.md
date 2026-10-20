# Architecture, verification and controls

Private main revision: `e68c59e6897ebc3d1fdb30df2ab390b083bdc596` · committed 2026-10-20T13:37:05+07:00.

Documentation only. No Solidity, application, backend or calculator source is published here. This is not an audit or a claim of explorer source verification. Live balances and current configuration: [Under the Hood](https://netnetintel.com/under-the-hood) and [Funded Pots](https://netnetintel.com/turfwar-funding).

Wallet-signed purchases → KeyShop → revenue router → earmarked player pots, supporter routes, buyback budget and reserve. Verified runs and summons → settlement publication → player claims.

Contracts enforce balances, permissions and claim execution. Backend services index chain events, reconcile tickets, verify replays and publish settlement data. Those services and anti-cheat implementation remain private. Public explanations do not make all settlement independently reproducible.

Current game administration is designed around the Team Safe and Timelock. Emergency pauses and delayed governance changes have different paths. Testnet governance delay is 10 minutes; the intended mainnet delay is 72 hours, but game mainnet is not deployed. Confirm current controllers and roles on chain.

Important dependencies include commitment/reveal integrity, keeper liveness, settlement operator correctness, root publication, oracles, external token behavior, conversion liquidity and governance. Source verification is an explorer property, not guaranteed by an address appearing here. No audit certification is implied.

[Contract directory](contracts/README.md)
