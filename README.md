# Wallaby Testnet

Meta info about the Wallaby testnet for FVM developers

![david-clode-ko-v55B2xOw-unsplash](https://user-images.githubusercontent.com/1017762/189190624-cb1179cd-4b1e-437c-947b-493ebd2568f0.png)
<br><sup><sub>photo by [David Clode on Unsplash](https://unsplash.com/@davidclode)<sup><sub>

&nbsp;

**Maintainer:** @f8-ptrk



**Genesis**:

- CAR File: `QmSuMh7J45Ywk8FM3pRUwpwa4VHhMGb1Kqfag4Y5ijnALT`
- Reset Timestamp: `2022-09-13T07:37:35Z`
- Genesis Block CID: `bafy2bzacedwlt256tdjowtpjgg776rrnvsg4jkhyn7e5y72q3yh4oe6rzkpg2`
- sha1 Digest: `d0f9c1c8b5fcd8c447f746bb5b694b2b12f20e88`

**Network parameters**:

- Supported Sector Sizes: `512 MiB` and `32 GiB` and `64 GiB`
- Consensus Miner Min Power: `16 GiB`
- Epoch Duration Seconds: `30`
- Expected Leaders per Epoch: `5`
- WindowPoSt Proving Period: `2880`
- WindowPoSt Challenge Window: `60`
- WindowPoSt Period Deadlines: `48`
- Pre-Commit Challenge Delay: `10`

**Bootstrap peers**:

```
/dns4/de0.bootstrap.wallaby.network/tcp/1337/p2p/12D3KooWHAvUVk5XuxSwi2dNLWbTDDRSGeHxMuWdQ3SQpRuNHbLz
/dns4/de1.bootstrap.wallaby.network/tcp/1337/p2p/12D3KooWBRqtxhJCtiLmCwKgAQozJtdGinEDdJGoS5oHw7vCjMGc
/dns4/ca0.bootstrap.wallaby.network/tcp/1337/p2p/12D3KooWCApBpUk7EX9pmEfyky1gKC6N2KJ74S1AwFfvnkDqw3pK
/dns4/sg0.bootstrap.wallaby.network/tcp/1337/p2p/12D3KooWLnYqr4hRoNHBJQVXsFGkDoKuoVfw5R2ASw1bHzrWU5Px
```

**FVM release**:

- [Selenium(r2)](https://github.com/filecoin-project/testnet-wallaby/issues/4)
- [Talc(r1)](https://github.com/filecoin-project/testnet-wallaby/issues/2)
- Lotus commit: [c54145e337b8e21e22ea9bb45006122d0e13aa49](https://github.com/filecoin-project/lotus/commit/c54145e337b8e21e22ea9bb45006122d0e13aa49)
- [List of FVM releases](https://github.com/filecoin-project/ref-fvm/issues/692)

**Resources**:

- Slack Channel for Updates: [#fil-net-wallaby-discuss](https://filecoinproject.slack.com/archives/C03KGBTJ0BY)
- Slack Channel for Questions: [#fil-net-wallaby-help](https://filecoinproject.slack.com/archives/C03KGBVJCKG)
- **Wallaby Docs**: [https://kb.factor8.io/en/docs/fil/wallabynet](https://kb.factor8.io/en/docs/fil/wallabynet)
- **Faucet**: https://wallaby.network/#faucet
- **Block Explorer**: [https://wallaby.filscan.io](https://wallaby.filscan.io)
- **JSON RPC API - Public Endpoints**:
  - Limited to all read API calls + `MPoolPush` (for sending already signed messages)
  - https://wallaby.node.glif.io/rpc/v0 (for stable API v0)
  - https://wallaby.node.glif.io/rpc/v1 (for new API v1 - see [API README](https://github.com/filecoin-project/lotus/blob/422f66776fa07827f2cfa9d2f8142ef29dcd2a95/api/README.md))
- **Wallaby SPs auto-accepting storage deals:**
  - See [Deal Miners section in the Wallaby Docs](https://kb.factor8.io/en/docs/fil/wallabynet#deal-miners)
- **Schedule**: 
  - Normally reset every Tuesday with [bleeding edge FEVM releases](https://github.com/filecoin-project/ref-fvm/issues/692)
  - Follow [#fil-net-wallaby-discuss](https://filecoinproject.slack.com/archives/C03KGBTJ0BY) for updates



<hr>

:warning: [TODO - SAMPLE INFO BELOW] :warning: 

**SPs auto-accepting storage deals** 

- todo @f8-ptrk, wait 24h before network is declared stable

- [Latest chain snapshot (pruned)](https://fil-chain-snapshots-fallback.s3.amazonaws.com/mainnet/minimal_finality_stateroots_latest.car)
- [Latest chain snapshot (full)](https://fil-chain-snapshots-fallback.s3.amazonaws.com/mainnet/complete_chain_with_finality_stateroots_latest.car)
- [Status page and incidents](https://filecoin.statuspage.io/)
- [Stats dashboard](https://stats.filecoin.io/)
- [Block explorer: Filscan](https://filscan.io/)
- [RPC Endpoints] - TODO

:warning: [TODO - SAMPLE INFO ABOVE] :warning: 
