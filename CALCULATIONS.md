# Formulas and worked examples

Private main revision: `cea11f0aca8152ed5b86384f6247c6a209c4466f` · committed 2026-10-20T09:51:53+07:00.

Documentation only. No Solidity, application, backend or calculator source is published here. This is not an audit or a claim of explorer source verification. Live balances and current configuration: [Under the Hood](https://netnetintel.com/under-the-hood) and [Funded Pots](https://netnetintel.com/turfwar-funding).

## Revenue

For raw token amount A and basis-point split b: allocation[i] = floor(A × b[i] / 10000). The last destination receives the remainder. Apply the same rule separately to each four-week reward allocation; dust is assigned once, never duplicated.

Example: 10,000 USDG sales in week 1, then 1,000 per week for seven weeks, then no further sales.

| Week | Sales (USDG) | Points funding | RWA funding |
| --- | --- | --- | --- |
| W1 | 10000 | 3000 | 500 |
| W2 | 1000 | 1800 | 300 |
| W3 | 1000 | 1350 | 225 |
| W4 | 1000 | 1140 | 190 |
| W5 | 1000 | 600 | 100 |
| W6 | 1000 | 600 | 100 |
| W7 | 1000 | 600 | 100 |
| W8 | 1000 | 600 | 100 |
| W9 | 0 | 300 | 50 |
| W10 | 0 | 150 | 25 |
| W11 | 0 | 60 | 10 |

## Player estimates

Eligible summon points = min(verified summon points, 1.5 × verified played Ranked points). Weekly eligible points combine played and capped summon points. A player's estimated points share uses eligible player points / total eligible points, subject to applicable pool rules and verification. Free mode does not earn paid points-pot entitlement.

Capsule weighted units use the square root of the Ranked key multiplier. USD per eligible unit = min(funded RWA USDG / all eligible weighted units, configured USD cap per unit). Player estimate = eligible units × USD per unit. Caps can leave money unallocated; do not redistribute it in an estimate without the contract rules.

## Supporter illustration

Weekly exposure budget ≤ 2% of opening capital. Applied top-up = exposure budget × utilization. Costs are capped by actual fee revenue. Illustrative net change = delivered supporter revenue − applied top-up − permitted costs. Annualizing one week is not a promised yield. A 5% sales allocation is revenue routing, not 5% interest.

The website's linked weekly-sales slider drives the four-week schedule, selected player pots and USDG supporter scenario. Player units, capital and utilization have separate controls. These controls never change live contracts.
