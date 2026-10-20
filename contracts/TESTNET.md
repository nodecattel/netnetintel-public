# Testnet game, clones and integrations

Private main revision: `ae5e4c12ba5ade1cd70292ec71f5d5be52f3df39` · committed 2026-10-20T10:22:08+07:00.

Documentation only. No Solidity, application, backend or calculator source is published here. This is not an audit or a claim of explorer source verification. Live balances and current configuration: [Under the Hood](https://netnetintel.com/under-the-hood) and [Funded Pots](https://netnetintel.com/turfwar-funding).

Chain ID: 46630. Clones and stand-ins are test assets; their presence does not imply mainnet value or safety.

| Contract | Group | Purpose | Explorer |
| --- | --- | --- | --- |
| WeeklyPool | Game economy | Weekly points settlement and claims | [0xabea96a8fee7dad8ae4ab54f2b19281033afb583](https://explorer.testnet.chain.robinhood.com/address/0xabea96a8fee7dad8ae4ab54f2b19281033afb583) |
| StockVault | Game economy | Capped capsule rewards, payout choices and claims | [0x495e2fa9d5d08c1437060fa181504757616227f3](https://explorer.testnet.chain.robinhood.com/address/0x495e2fa9d5d08c1437060fa181504757616227f3) |
| WsNetSeller | Game economy | Guarded wsNET to USDG conversion | [0x2b7c6fd3c107748f7641720685b7b17d294282e7](https://explorer.testnet.chain.robinhood.com/address/0x2b7c6fd3c107748f7641720685b7b17d294282e7) |
| StabilizationReserve | Game economy | Liquid reserve, separate from claims | [0xdd363c85c60811d375efe03ac391cb9e01633f43](https://explorer.testnet.chain.robinhood.com/address/0xdd363c85c60811d375efe03ac391cb9e01633f43) |
| BountyEscrow | Game economy | Funded qualified bounties and claims | [0xb2776d1aa7fde2aa9ce6e2e94e7a9c5e21beb7b3](https://explorer.testnet.chain.robinhood.com/address/0xb2776d1aa7fde2aa9ce6e2e94e7a9c5e21beb7b3) |
| AtomicBuyback | Game economy | Atomic NET market buy, inverse redemption and burn checks | [0x16531e05feb76c4e6b65c2521f3c9e798f9127da](https://explorer.testnet.chain.robinhood.com/address/0x16531e05feb76c4e6b65c2521f3c9e798f9127da) |
| RevenueRouter | Game economy | Key-sale split and four-week funding schedule | [0x604001677399997da32cb3972ff0a70cafe09447](https://explorer.testnet.chain.robinhood.com/address/0x604001677399997da32cb3972ff0a70cafe09447) |
| KeyShop | Game economy | Key purchases, balances, holds and spending | [0x6ea002b5452f01ff22fa62b48e8c7bb754896bed](https://explorer.testnet.chain.robinhood.com/address/0x6ea002b5452f01ff22fa62b48e8c7bb754896bed) |
| SummonDesk | Game economy | Commit/reveal tickets, tier settlement and key reclaim | [0x149bf6ab0359bd7b38db7ce9316cf3856e32be55](https://explorer.testnet.chain.robinhood.com/address/0x149bf6ab0359bd7b38db7ce9316cf3856e32be55) |
| GameConfig | Game infrastructure | Versioned economic settings | [0x1E7711A0819Da8e9022F06167fc3fF9984939a2e](https://explorer.testnet.chain.robinhood.com/address/0x1E7711A0819Da8e9022F06167fc3fF9984939a2e) |
| GameTreasury | Game infrastructure | Recovered buyback USDG and treasury assets; yield routing pending review | [0x617b343fed59f1d02E2f990Bbe78a124ecCA63Ba](https://explorer.testnet.chain.robinhood.com/address/0x617b343fed59f1d02E2f990Bbe78a124ecCA63Ba) |
| TimelockController | Game infrastructure | Delayed game administration | [0xbE887E98f165E4fB09091A669CCa2f585c677cE7](https://explorer.testnet.chain.robinhood.com/address/0xbE887E98f165E4fB09091A669CCa2f585c677cE7) |
| LockVault | Game infrastructure | wsNET lock positions and Summon eligibility | [0x94f63553626c82E14B4b5938E63eeFB4B1029E8e](https://explorer.testnet.chain.robinhood.com/address/0x94f63553626c82E14B4b5938E63eeFB4B1029E8e) |
| FoundingPass | Game infrastructure | Founder Signet eligibility | [0xD040cfb1127B88B6854e6f45Ab72B5BFB93274F6](https://explorer.testnet.chain.robinhood.com/address/0xD040cfb1127B88B6854e6f45Ab72B5BFB93274F6) |
| WsNetBuyer | Game infrastructure | NET purchase, staking and wrapping adapter | [0xf92e89e84dECcE643221e3802e14aA702547FBfc](https://explorer.testnet.chain.robinhood.com/address/0xf92e89e84dECcE643221e3802e14aA702547FBfc) |
| NetUnwrapper | Game infrastructure | Unwrap and unstake adapter | [0x087fba79612B57750393837eD9509951D98Ba0aA](https://explorer.testnet.chain.robinhood.com/address/0x087fba79612B57750393837eD9509951D98Ba0aA) |
| Team Safe | Testnet infrastructure | Test multisig; not the mainnet NetNet Safe | [0x294388369A097c8E5c5C834e86D64925C5399846](https://explorer.testnet.chain.robinhood.com/address/0x294388369A097c8E5c5C834e86D64925C5399846) |
| USDG Supporter Vault | Supporter pilots | ERC-4626 shares and bounded top-up exposure | [0x413E967d3057516861e2662fc122941A74Ea69a1](https://explorer.testnet.chain.robinhood.com/address/0x413E967d3057516861e2662fc122941A74Ea69a1) |
| USDG Supporter Reward Escrow | Supporter pilots | Separately reserved player top-ups | [0x22db9a28809007Cfd4D9E9c107DBCa2bD028451F](https://explorer.testnet.chain.robinhood.com/address/0x22db9a28809007Cfd4D9E9c107DBCa2bD028451F) |
| wsNET Supporter Vault | Supporter pilots | ERC-4626 shares and bounded top-up exposure | [0x6340D1D4Dc3Ab722809dAe41363c47B711F29C7b](https://explorer.testnet.chain.robinhood.com/address/0x6340D1D4Dc3Ab722809dAe41363c47B711F29C7b) |
| wsNET Supporter Reward Escrow | Supporter pilots | Separately reserved player top-ups | [0x36f06d21df5313665202B8b908a00dF241ffb22c](https://explorer.testnet.chain.robinhood.com/address/0x36f06d21df5313665202B8b908a00dF241ffb22c) |
| TurfWar Gear | Game infrastructure | Game gear NFTs and ownership provenance | [0xa2f7843667a7448db4cd3eec22e664b74b5233c9](https://explorer.testnet.chain.robinhood.com/address/0xa2f7843667a7448db4cd3eec22e664b74b5233c9) |
| USDG | Testnet stand-ins | TestUSDG stand-in with permissionless drip(); not real USDG | [0xD8601E6476c5B42128D7CF64dAc4C1d58eF47A82](https://explorer.testnet.chain.robinhood.com/address/0xD8601E6476c5B42128D7CF64dAc4C1d58eF47A82) |
| NET | NetNet testnet clones | Reserve-token bytecode clone; test assets only | [0x6f7ADC41e49c77617563528D59eC7D78b030D7aC](https://explorer.testnet.chain.robinhood.com/address/0x6f7ADC41e49c77617563528D59eC7D78b030D7aC) |
| sNET | NetNet testnet clones | Rebasing staked-NET bytecode clone | [0xab6add8E7d9CE585572777cEbcb5e1e32906Ce5d](https://explorer.testnet.chain.robinhood.com/address/0xab6add8E7d9CE585572777cEbcb5e1e32906Ce5d) |
| wsNET | NetNet testnet clones | Non-rebasing wrapped staked-NET clone | [0xcf719655e65c196bdEbb7d4390D83c80F3acAfbF](https://explorer.testnet.chain.robinhood.com/address/0xcf719655e65c196bdEbb7d4390D83c80F3acAfbF) |
| Staking | NetNet testnet clones | Stake, unstake and epoch rebase clone | [0xC99a903593EC6AE3469ba1016cEa84545C2767d2](https://explorer.testnet.chain.robinhood.com/address/0xC99a903593EC6AE3469ba1016cEa84545C2767d2) |
| Treasury | NetNet testnet clones | Protocol reserve and backing-accounting clone | [0x0e42ce1f915f884D77e585f63E0a9468E3DA5985](https://explorer.testnet.chain.robinhood.com/address/0x0e42ce1f915f884D77e585f63E0a9468E3DA5985) |
| PairNetUsdg | Testnet infrastructure | Testnet NetNet integration · test assets | [0x26d00306137EaBF461702Ba8dEbDFBA71cCBc0D0](https://explorer.testnet.chain.robinhood.com/address/0x26d00306137EaBF461702Ba8dEbDFBA71cCBc0D0) |
| PairOracle | NetNet testnet clones | Canonical NET/USDG TWAP oracle clone | [0xc816673CD7C5411F86ce17Cc10254C5081f13Bc8](https://explorer.testnet.chain.robinhood.com/address/0xc816673CD7C5411F86ce17Cc10254C5081f13Bc8) |
| Router | Testnet infrastructure | Testnet NetNet integration · test assets | [0xF41E290877085376Cf8baD5E9c7bEB68EC50Aed4](https://explorer.testnet.chain.robinhood.com/address/0xF41E290877085376Cf8baD5E9c7bEB68EC50Aed4) |
| InverseBond | NetNet testnet clones | Inverse-bond standing bid and NET burn clone | [0xa26411050fEcf9274677a9cdC678eb4FEB3D27A8](https://explorer.testnet.chain.robinhood.com/address/0xa26411050fEcf9274677a9cdC678eb4FEB3D27A8) |
| TSLA token | Stock rewards | Supported test stock payout token | [0x23adE52Bb836A5b3B1E108c8Bbc8760D568e43Eb](https://explorer.testnet.chain.robinhood.com/address/0x23adE52Bb836A5b3B1E108c8Bbc8760D568e43Eb) |
| TSLA feed | Stock rewards | Stock pricing input | [0x539352f5494f15c4915FFa8E8ACBee77318604a6](https://explorer.testnet.chain.robinhood.com/address/0x539352f5494f15c4915FFa8E8ACBee77318604a6) |
| SPCX token | Stock rewards | Supported test stock payout token | [0xE1493cA8f181f7745B719DbC84fa0cFd5b630426](https://explorer.testnet.chain.robinhood.com/address/0xE1493cA8f181f7745B719DbC84fa0cFd5b630426) |
| SPCX feed | Stock rewards | Stock pricing input | [0x37660A7b1Df5c5593E112035d44bBd8A1713e603](https://explorer.testnet.chain.robinhood.com/address/0x37660A7b1Df5c5593E112035d44bBd8A1713e603) |
| NVDA token | Stock rewards | Supported test stock payout token | [0x0b72B6A0E1CA5D85BA16754FbAA51a79806e8F37](https://explorer.testnet.chain.robinhood.com/address/0x0b72B6A0E1CA5D85BA16754FbAA51a79806e8F37) |
| NVDA feed | Stock rewards | Stock pricing input | [0xaD71f4958665AF1b525E3CE2E96f768F45e7dEf2](https://explorer.testnet.chain.robinhood.com/address/0xaD71f4958665AF1b525E3CE2E96f768F45e7dEf2) |
| MSFT token | Stock rewards | Supported test stock payout token | [0x638F101064681d595D614D44342133dA45314B1F](https://explorer.testnet.chain.robinhood.com/address/0x638F101064681d595D614D44342133dA45314B1F) |
| MSFT feed | Stock rewards | Stock pricing input | [0x61f80095118359C843C9F670bac2f5b9a5aB71D0](https://explorer.testnet.chain.robinhood.com/address/0x61f80095118359C843C9F670bac2f5b9a5aB71D0) |
| GOOGL token | Stock rewards | Supported test stock payout token | [0x78036D4968e6Bf64777897FDA3962879ddC9d024](https://explorer.testnet.chain.robinhood.com/address/0x78036D4968e6Bf64777897FDA3962879ddC9d024) |
| GOOGL feed | Stock rewards | Stock pricing input | [0x3D7E385bFeac40C459C3E8317eBcFE1Dcb2A4d6f](https://explorer.testnet.chain.robinhood.com/address/0x3D7E385bFeac40C459C3E8317eBcFE1Dcb2A4d6f) |
| AAPL token | Stock rewards | Supported test stock payout token | [0xcE3904f5CfbD0F94835d64A02A855eb95c2cC8bE](https://explorer.testnet.chain.robinhood.com/address/0xcE3904f5CfbD0F94835d64A02A855eb95c2cC8bE) |
| AAPL feed | Stock rewards | Stock pricing input | [0x3DF0433A933d1851b60805C698aB1e7f19c724a9](https://explorer.testnet.chain.robinhood.com/address/0x3DF0433A933d1851b60805C698aB1e7f19c724a9) |
| COIN token | Stock rewards | Supported test stock payout token | [0xA11B4547430790E6a7f75360b42951C3Ea1944A3](https://explorer.testnet.chain.robinhood.com/address/0xA11B4547430790E6a7f75360b42951C3Ea1944A3) |
| COIN feed | Stock rewards | Stock pricing input | [0x4f5dB031589c535AFaEed8147180a997ABB17Ad1](https://explorer.testnet.chain.robinhood.com/address/0x4f5dB031589c535AFaEed8147180a997ABB17Ad1) |
| BondDepository | NetNet testnet clones | Primary bond-subscription clone | [0x68a5291bE258fA83F31e72A418da07d7288380e7](https://explorer.testnet.chain.robinhood.com/address/0x68a5291bE258fA83F31e72A418da07d7288380e7) |
| Distributor | NetNet testnet clones | Epoch emission-formula clone | [0x372F521cFC1fe7C21F0d627d17081669875A7252](https://explorer.testnet.chain.robinhood.com/address/0x372F521cFC1fe7C21F0d627d17081669875A7252) |
| ShareCertificate | NetNet testnet clones | Founding-share certificate clone | [0x53dc21648b76ac62Bf18639515Bc2f5880fD5ef8](https://explorer.testnet.chain.robinhood.com/address/0x53dc21648b76ac62Bf18639515Bc2f5880fD5ef8) |
| GenesisBond | NetNet testnet clones | Founding-subscription clone; check subscription window before use | [0x0390943018454a024Fc955846b912Ed36DaF2F63](https://explorer.testnet.chain.robinhood.com/address/0x0390943018454a024Fc955846b912Ed36DaF2F63) |
| MorphoVault | Testnet stand-ins | Simplified yield-vault stand-in; not the production Morpho vault | [0x55f2566BEd9a1b2f137c00fdCD84E40854eF6eB3](https://explorer.testnet.chain.robinhood.com/address/0x55f2566BEd9a1b2f137c00fdCD84E40854eF6eB3) |
| PairNetWeth | Testnet infrastructure | Test liquidity infrastructure | [0x759acb9222039cD37d3928906c9E0B7013d773B1](https://explorer.testnet.chain.robinhood.com/address/0x759acb9222039cD37d3928906c9E0B7013d773B1) |
| PremiumSeller | NetNet testnet clones | Premium NET sale clone | [0x3C048bE7798395f0D76579472298BF60d477B581](https://explorer.testnet.chain.robinhood.com/address/0x3C048bE7798395f0D76579472298BF60d477B581) |
| TaxCollector | NetNet testnet clones | Trading-fee collection clone | [0x1C971dC9eFAb19CC4AdDdA5002Ad433514621827](https://explorer.testnet.chain.robinhood.com/address/0x1C971dC9eFAb19CC4AdDdA5002Ad433514621827) |
| pTEAM | NetNet testnet clones | Team option exercise clone | [0x21FFEEB45e94664b23B6a0BA22d0eF0A46Ed0D9C](https://explorer.testnet.chain.robinhood.com/address/0x21FFEEB45e94664b23B6a0BA22d0eF0A46Ed0D9C) |
| UniswapV2Factory | Testnet infrastructure | Test liquidity infrastructure | [0x497C689eE59e79b1B42deCa5f0ffbC8A780BD3b3](https://explorer.testnet.chain.robinhood.com/address/0x497C689eE59e79b1B42deCa5f0ffbC8A780BD3b3) |
| UniswapV3Factory | Testnet infrastructure | Test liquidity infrastructure | [0x8E2a216693A403347d1e34B0b986940cca1D7bd7](https://explorer.testnet.chain.robinhood.com/address/0x8E2a216693A403347d1e34B0b986940cca1D7bd7) |
| WETH | Testnet infrastructure | Test wrapped ETH deployment | [0x05bd6EB5F6c521f33F901183022aB74c012AbBf3](https://explorer.testnet.chain.robinhood.com/address/0x05bd6EB5F6c521f33F901183022aB74c012AbBf3) |
