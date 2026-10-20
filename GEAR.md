# TurfWar Gear · loot, enhancement and critical hits

Private main revision: `22801d4eadd8ab159a300afd109cf69743f44dae` · committed 2026-10-20T11:31:10+07:00.

Documentation only. No Solidity, application, backend or calculator source is published here. This is not an audit or a claim of explorer source verification. Live balances and current configuration: [Under the Hood](https://netnetintel.com/under-the-hood) and [Funded Pots](https://netnetintel.com/turfwar-funding).


The replacement is testnet-only. Production activation requires the collection's
Safe/Timelock permission, matching game/verifier release and the server's v2 switch.
Existing rewards, NFTs and recorded run engines remain available.

## Boss loot

The three district-clear bosses roll an additional gear container at 8%, 12% and
18%, alongside the existing capsule reward from the same kill. Break the container,
collect its chest, then open it in Workshop → Loot after the run verifies. The
container cannot reveal a design, class or rarity before opening. A short post-boss
salvage window permits pickup; uncollected loot carries into the next district.
Collected chests remain earned after defeat. Free and Ranked use the same odds;
Summon does not earn boss gear yet.

Accounts and linked wallets share a five-chest UTC-day allowance. Verified pickup
allocation is atomic and idempotent. Opening an earned chest burns no keys; the
player pays network gas. Duplicate items are allowed and minted gear is tradable.

Successful boss openings roll 90% Base / 10% Enhanced, never exclusive NET Gear or
Artifact class. Each of the 12 item designs has equal conditional probability.
Rarity probabilities are Common 45%, Uncommon 27.5%, Rare 16.25%, Epic 7.5%,
Legendary 3%, Mythic 0.75%, using integer thresholds over the proof stream.

## Four classes and fixed starting gains

Base → NET Gear → Enhanced → Artifact are separate from rarity. The highest rarity
is Mythic. Within any slot, every Artifact exceeds every Enhanced item.

| Class | Common to Mythic share of slot budget |
| --- | --- |
| Base | 10–20% |
| NET Gear, official NFT holders only | 25–40% |
| Enhanced | 45–60% |
| Artifact, reviewed weekly prizes | 70–100% |

| Slot | Maximum primary starting gain | Additional crit budget |
| --- | --- | --- |
| Head | +20% original HP | +5 percentage points |
| Chest | +50% original HP | — |
| Back | +30% original HP | — |
| Feet | +35% original speed | — |
| Weapon | +100% original weapon damage | +10 percentage points |
| Off-hand | +20 percentage points armor | — |
| Accessory | +100% original pickup radius | +5 percentage points |

Multiply each slot budget by its class/rarity share. The combined loadout cannot
exceed +100% of any original stat, +20 armor points or 20% total crit chance.
These are ceilings, not guaranteed gains. Founder Signet remains Magnet I (+30%
pickup), occupies Accessory and grants no crit. Existing v1 native NFTs retain
their original fixed item bonuses.

The baseline crit chance is zero. Normal crit damage is 1.5×, displayed in yellow.
Each attack shares one seeded roll across its targets, piercing and repeated
contacts. 100X keeps its special critical damage multiplier; its intrinsic chance
and gear together are capped at 20%. The replay verifier uses the same math.
Gear additions freeze against original starting values, do not scale with level-up
multipliers, and add no XP, score or RWA multiplier.

## Weekly Artifact prizes

Each final verified Ranked top-three winner receives one account-bound Artifact
chest after explicit weekly review and the settlement challenge window. Opening
rolls one tradable Artifact-class item. Weekly prizes are outside the boss daily
cap. Awards bind the canonical account, week and final on-chain settlement root.
Retries cannot issue a second chest or replace an already awarded root. A tie
spanning the third-place cutoff holds the prize allocation for reviewed resolution.

## Enhancement

Costs by Common / Uncommon / Rare / Epic / Legendary / Mythic:
**2 / 3 / 4 / 6 / 8 / 12 keys**.

TurfWar Base is burned atomically with the key charge to mint Enhanced. An official
NET Gear source stays intact but is permanently marked used for enhancement.
Earlier official-source enhancement history is checked before issuing a new
voucher. Enhanced and Artifact cannot enhance again. Original NET Gear unlocks
require current official mainnet ownership, including while playing on testnet.
A transfer during a run leaves that run's frozen snapshot intact; the next run
rechecks ownership and removes missing items.

## What a chest proof establishes

1. The backend qualifies a chest from a verified run or reviewed final settlement.
2. Provable supplies a fresh commitment before the player's opening transaction.
3. The opening binds the player, account, reward, commitment and fresh client salt.
4. Only after that transaction lands does the keeper request the reveal.
5. The contract checks the revealed seed against the commitment and applies the
   existing Provable HMAC stream math to domain-separated design/rarity/class rolls.
6. One reward ID can mint once. A pending opening retains its original commitment;
   outages retry its status and reveal rather than rerolling.

The downloadable proof includes the collection, chain, reward ID, token ID,
commitment, client seed, revealed server seed and randomness after settlement.
This proves the committed roll. Qualification and cross-chain NET ownership still
rely on the disclosed server attester; this is not a fully trustless bridge.

Inspect the current collection and governance through [the public contract directory](contracts/TESTNET.md). Mainnet is not activated.
