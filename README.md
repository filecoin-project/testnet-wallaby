# Wallaby Testnet

Meta info about the Wallaby testnet for FVM developers

![david-clode-ko-v55B2xOw-unsplash](https://user-images.githubusercontent.com/1017762/189190624-cb1179cd-4b1e-437c-947b-493ebd2568f0.png)
<br><sup><sub>photo by [David Clode on Unsplash](https://unsplash.com/@davidclode)<sup><sub>

&nbsp;

## Quickstart

1. Add the Wallaby testnet to your wallet (e.g. MetaMask).
    - Go to https://chainlist.org/chain/31415
    - Click on "Connect wallet"
2. Create a new account in MetaMask to use with Filecoin.
3. Use the [faucet](https://wallaby.network/#faucet) to draw funds to your Ethereum address (it will be converted behind the scenes to a Filecoin f4 address)
4. Follow the transaction in one of the recommended Wallaby testnet explorers:
    - https://wallaby.filfox.info/en
    - https://explorer.glif.io/ (select Wallaby from the networks dropdown)
5. Your account is now funded and can be used in Ethereum tools such as Hardhat, Foundry, Remix, etc.

## Technical details

**Maintainer:** @f8-ptrk

**Genesis**:

- CAR File: `Qmd62btfm43bsS2doYEKbWnMstKQCY5vwoa8ScF1qVDuYX`
- Reset Timestamp: `2022-12-20T14:29:06Z`
- Genesis Block CID: `bafy2bzacebha2xerd4kax7atfefc5idqdjo5wnacx4r2dodhq32zqncuukhna`
- sha1 Digest: `1266623f65b988874ddcb576929418dd985e574a`

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

- [FVM M2.1 Sapphire (r09)](https://github.com/filecoin-project/ref-fvm/issues/940)
- Lotus commit: [373b8b3517c6ade6f9d346bfe3c0af30007f2b47](https://github.com/filecoin-project/lotus/commit/373b8b3517c6ade6f9d346bfe3c0af30007f2b47)
- [List of FVM releases](https://github.com/filecoin-project/ref-fvm/issues/692)

**Resources**:

- Slack Channel for Updates: [#fil-net-wallaby-discuss](https://filecoinproject.slack.com/archives/C03KGBTJ0BY)
- Slack Channel for Questions: [#fil-net-wallaby-help](https://filecoinproject.slack.com/archives/C03KGBVJCKG)
- **Wallaby Docs**: [https://kb.factor8.dev/docs/filecoin/testnets/wallaby](https://kb.factor8.dev/docs/filecoin/testnets/wallaby)
- **Faucet**: https://wallaby.network/#faucet
- **Block Explorers**:
  - [https://wallaby.filscan.io](https://wallaby.filscan.io)
  - [https://explorer.glif.io/actor/?network=wallaby](https://explorer.glif.io/actor/?network=wallaby)
  - [https://wallaby.filfox.info/en](https://wallaby.filfox.info/en)
  - [https://beryx.zondax.ch/](https://beryx.zondax.ch/)
- **Filecoin CID Checker**: [https://wallaby.filecoin.tools](https://wallaby.filecoin.tools/) - check your deal CID’s storage status
- **JSON RPC API - Public Endpoints**:
  - Limited to all read API calls + `MPoolPush` (for sending already signed messages)
  - https://wallaby.node.glif.io/rpc/v0 (for stable API v0)
  - https://wallaby.node.glif.io/rpc/v1 (for new API v1 - see [API README](https://github.com/filecoin-project/lotus/blob/422f66776fa07827f2cfa9d2f8142ef29dcd2a95/api/README.md))
  - web socket endpoint: wss://wss.wallaby.node.glif.io/apigw/lotus/rpc/v0
- **Wallaby SPs auto-accepting storage deals:**
  - See [Deal Miners section in the Wallaby Docs](https://kb.factor8.dev/docs/filecoin/testnets/wallaby#deal-miners)
- **Schedule**: 
  - Normally reset every Tuesday with [bleeding edge FEVM releases](https://github.com/filecoin-project/ref-fvm/issues/692)
  - Follow [#fil-net-wallaby-discuss](https://filecoinproject.slack.com/archives/C03KGBTJ0BY) for updates
- **MetaMask** (HowTo): 
  - Open MetaMask and add a new network:
    - Name: Filecoin Wallaby
    - RPC URL: https://wallaby.node.glif.io/rpc/v0 (once the public RPC has been updated, otherwise use appropriate private URL - **please see the note below**)
    - ChainID: [**31415**](https://github.com/ethereum-lists/chains/blob/master/_data/chains/eip155-31415.json) (Wallaby's )
    - Currency symbol: tFIL (Test FIL).
  - Create a new account in MetaMask to use with Filecoin.
  - (OPTIONAL - the faucet accepts 0x style addresses now) Go to https://explorer.glif.io/ethereum/, and select the account to see its f4 address.
  - Use the [faucet](https://wallaby.network/#faucet) to draw funds to your f4 (0x style addresses are translated automatically to f4's in the backend) or alternatively use `lotus send` to transfer funds to the f4 address.
  - Wait until the transaction process, and verify that the funds appear in MetaMask.
  - Create another new account in MetaMask, (optional) obtain its f4 address again.
  - Use MetaMask to send funds from your first account to your second account. 
  - **Notes on MM**
    - Note that you may need to increase the gas limit manually because there's something strange going on with gas estimation at the moment.
  - **Note on GLIF**:
    - The GLIF explorer seems to have some problems with f4 addresses right now, please refer to the #fil-net-wallaby-discuss for questions/solutions 


<hr>

:warning: [TODO - SAMPLE INFO BELOW] :warning: 

- [Latest chain snapshot (pruned)](https://fil-chain-snapshots-fallback.s3.amazonaws.com/mainnet/minimal_finality_stateroots_latest.car)
- [Latest chain snapshot (full)](https://fil-chain-snapshots-fallback.s3.amazonaws.com/mainnet/complete_chain_with_finality_stateroots_latest.car)
- [Status page and incidents](https://filecoin.statuspage.io/)
- [Stats dashboard](https://stats.filecoin.io/)
- [Block explorer: Filscan](https://filscan.io/)

:warning: [TODO - SAMPLE INFO ABOVE] :warning: 
