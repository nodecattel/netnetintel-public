# TurfWar Gear · loot, enhancement and critical hits

Private main revision: `6a4b028f766445f055c5a0d217fa7fd2aa18f894` · committed 2026-10-29T15:11:40+07:00.

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

# Testnet gear gameplay balance 3

The owner approved stronger starting bonuses immediately on testnet. Only new authoritative run snapshots tagged `balanceVersion: 3` receive this tuning. Existing native v1 items retain their original item rules; Founder Signet retains Magnet I (+30% pickup). Existing recorded runs and their archived verifier engines are preserved. Summon still receives no gear bonuses.

## Collection and mint rules

All 12 designs can roll independently at Common, Uncommon, Rare, Epic, Legendary and Mythic. Base, Enhanced and Artifact each have 72 combinations (216 total). Official NET Gear remains an ownership entitlement derived from the actual mainnet collection, not a game drop or invented rarity. District bosses retain their 8/12/18% chest odds, five-per-day account/wallet quota and 90% Base / 10% Enhanced opening split. Artifact remains reviewed weekly Ranked top-three loot.

Existing deployed `GearCollectionV2` already supports these design/rarity combinations. Its mint-time `startingBonus`, `criticalBonus` and metadata `effects` are immutable v2 reference values. The new testnet game tuning is separate and explicitly labelled in the Workshop and public collection manifest; this update does not claim those Solidity methods changed. No collection migration, mint-price change or mainnet deployment occurs.

## Starting gains

Each design has a different profile. Multiply each profile’s maximum by the class/rarity factor: Base 25–40%, NET 45–60%, Enhanced 65–80%, Artifact 85–100%, linearly over six rarities. Stronger classes therefore stay ahead for the same design. Armor and crit are percentage points; other gains are percentages of original starting stats.

| Design | Maximum profile at Artifact Mythic |
|---|---|
| Transit Pass | +90% pickup, +12% speed, +4 points crit |
| Nightshift Flask | +35% health, +12 points armor |
| Runner Boots | +75% speed, +20% health |
| Neural Headset | +25% health, +20% damage, +6 points crit |
| Streetguard Jacket | +75% health, +10 points armor |
| Arc-Rail Blade | +100% damage, +12 points crit |
| Signal Collar | +45% health, +25% speed, +4 points crit |
| Scout Visor | +20% health, +35% pickup, +10 points crit |
| Encrypted Terminal | +20 points armor, +25% damage, +4 points crit |
| Authority Core | +100% pickup, +20% damage, +8 points crit |
| Escape Pack | +45% health, +20% speed, +25% pickup |
| Medtech Pulse Tool | +85% damage, +35% health, +8 points armor |

Full seven-slot loadouts cap each HP/speed/damage/pickup gain at +100%, armor at +20 points, and total crit chance at 20%. Normal crit remains 1.5×. Bonuses are fixed starting additions, not multiplicative level-up scaling, XP, score or reward multipliers.

The public discovery catalog lives at `/turfwar-gear/collection-manifest.json`. Discovery never implies ownership. Loadout ownership is checked before every run, so transferred items lose eligibility before the next run.

## Presentation

Back Alleys, Velvet Strip and Quiet Harbor use matching breakable containers, collectibles, summary art and opening videos. Reviewed Artifact chests use a separate opening. The enhancement forge composites the actual held source artwork and the verified minted Enhanced item; it cannot pick a different outcome or submit another transaction on replay. Rejected wallet requests never start a success reveal.


## New collection: account-bound shop boxes and Artifact balance v4

Street costs 3 keys: Common 65%, Uncommon 25%, Rare 10%. Elite costs 5 keys: Uncommon 50%, Rare 30%, Epic 15%, Legendary 5%. Apex costs 10 keys: Rare 50%, Epic 30%, Legendary 17%, Mythic 3%. Enhanced chances are independently 10% / 25% / 50%; other outcomes are Base. No purchased box can mint official NET Gear or Artifact.

Purchase burns keys once and records an account-bound chest. The chest has no NFT transfer method. Opening later commits with Provable, waits for the wallet transaction, reveals the same commitment and mints a tradable NFT. A failed or interrupted screen must recover that original purchase/opening; it must not charge or roll again. Opening costs no additional keys; both transactions use network gas. Paid boxes are separate from the five-per-day earned boss limit. Artifact remains a reviewed weekly Ranked top-three prize.

Key spending does not create a second revenue split: sales revenue was allocated when the keys were bought. The new collection declares a 5% resale royalty to the game treasury through ERC-2981. Marketplaces decide whether they enforce it; direct NFT transfers do not charge an automatic royalty. Only actually received royalties count as treasury income. Earlier NFTs are unchanged.

New collection snapshots explicitly use balanceVersion 4. Base, NET and Enhanced keep the existing v3 design profiles. Artifact has stronger slot profiles: its primary bonus reaches +100% of original HP, speed, damage or pickup at Mythic, or +20 armor points for Off-hand. Common–Mythic Artifact factors are 85 / 88 / 91 / 94 / 97 / 100% of that design's profile. Secondary effects vary by design. Seven-slot totals still cap at +100% per percentage stat, +20 armor points and 20% total crit chance. There is no level scaling, XP, score or reward multiplier.

Sovereign Mythic Artifact artwork marks the new top set. Earlier NFTs retain original artwork, balances and ownership checks; pending V2 reveals keep their original contract and proof.

