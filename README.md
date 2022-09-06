# Wallaby Testnet
Meta info about the Wallaby testnet for FVM developers

**Maintainer:** @f8-ptrk



**Genesis**:

- CAR File: `QmTvjvodwoCndP7DWUJeHEQ2sSCwZpxx8T5DoL1e612oiA`
- Reset Timestamp: `2022-09-06T15:22:45Z`
- Genesis Block CID: `bafy2bzaceaxkepuvjenqk7go7iemehzffdb3bv46ib4njz2je6hp5poyysa46`
- sha1 Digest: `6b502b70d87791a5009bb48775de19d0c02d3e7f`

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
- Lotus commit: [94895fbdf0f7a970e3c4a1a111172d7ddfc50e12](https://github.com/filecoin-project/lotus/commit/94895fbdf0f7a970e3c4a1a111172d7ddfc50e12)
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
