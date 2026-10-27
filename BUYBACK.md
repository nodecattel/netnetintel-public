# Guarded buyback and the NET connection

Private main revision: `685a25c3912de47c9e734ae343a600f027dcc381` · committed 2026-10-27T11:17:40+07:00.

Documentation only. No Solidity, application, backend or calculator source is published here. This is not an audit or a claim of explorer source verification. Live balances and current configuration: [Under the Hood](https://netnetintel.com/under-the-hood) and [Funded Pots](https://netnetintel.com/turfwar-funding).

The buyback allocation is initially 5% of key-sale revenue. The intended atomic route buys NET from market liquidity, then redeems it through NetNet's inverse-bond standing bid. NetNet receives and burns NET; recovered USDG returns to the game treasury. It is not a second pot contribution unless subsequently routed there.

Execution must recover the spent USDG plus the configured cost floor after fees, taxes and slippage. Otherwise the budget carries forward. Availability, liquidity, stale prices and configuration can prevent execution. A budget allocation is not proof that a burn has occurred or that profit is guaranteed. wsNET-funded shares require guarded conversion to USDG.

The current game treasury destination is not automatically the new weekly pool; do not count its income twice. Dashboard mainnet integrations read NetNet contracts and indexed chain events. Testnet clones and stand-ins are separately labelled, and tNET is a valueless futures test token, not redeemable wsNET.

[NetNet buyback documentation](https://docs.netnet.capital/treasury#the-buyback-program-inverse-bonds--the-standing-bid) · [Current adapter](contracts/TESTNET.md)
