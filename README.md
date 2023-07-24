:warning: The Hyperspace Testnet has been **discontinued** as of May 31, 2023. :warning:

Please use the [Calibration testnet](https://github.com/filecoin-project/testnet-calibration/blob/main/README.md).

Wallaby has been shut down until further notice and Hyperspace is the main testnet for Filecoin developers and testing FEVM releases. 

In the future, Wallaby will be used for testing bleeding-edge Wasm FVM releases (see the FVM Roadmap at https://fvm.filecoin.io).

# Wallaby Testnet

Meta info about Wallaby Weekly, a *bleeding edge* testnet for FVM development

- Not sure which testnet to use? Start with **[Hyperspace](https://github.com/filecoin-project/testnet-hyperspace)** - a stable testnet for Filecoin developers. **Wallaby is only for future experimental releases.**

- [Info about all testnets](https://github.com/filecoin-project/FIPs/discussions/544)

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

**Maintainer:** offline, unmaintained

**Genesis**:

- CAR File: `QmavrNRhTMbUNFtSJA6VVMMcSyCwQzUpJbSPRjZzKjy3Jg`
- Reset Timestamp: `2023-01-09T14:54:09Z`
- Genesis Block CID: `bafy2bzaceaq7a2nole6qaje33tydbvumeykjs4vjh2sh7hunsxwdsblpibxf2`
- sha1 Digest: `104a283cf7f3e805790c1e4fc02e50ed0f673981`

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

```

**FVM release**:

- [FVM M2.1 Carbonado (r10)](https://github.com/filecoin-project/ref-fvm/issues/1052)
- Lotus commit: [f2d5afc09431daea43291c52e38945b3147a7079](https://github.com/filecoin-project/lotus/commit/f2d5afc09431daea43291c52e38945b3147a7079)
- [List of FVM releases](https://github.com/filecoin-project/ref-fvm/issues/692)

**Resources**:

- Slack Channel for Updates: [#fil-net-wallaby-discuss](https://filecoinproject.slack.com/archives/C03KGBTJ0BY)

- **Wallaby Docs**:
- **Faucet**: 
- **Block Explorers**:
  - [https://wallaby.filscan.io](https://wallaby.filscan.io)
  - [https://explorer.glif.io/actor/?network=wallaby](https://explorer.glif.io/actor/?network=wallaby)
- **Filecoin CID Checker**: [https://wallaby.filecoin.tools](https://wallaby.filecoin.tools/) - check your deal CID’s storage status. This is **not a real-time** application and refreshes every 5 minutes.
- If you want to play with marketdeals on your own you can access them directly [here](https://marketdeals-wallaby.s3.ap-northeast-1.amazonaws.com/StateMarketDeals.json)

- **JSON RPC API - Public Endpoints**:
  - Limited to all read API calls + `MPoolPush` (for sending already signed messages)
  - https://wallaby.node.glif.io/rpc/v0 (for stable API v0)
  - https://wallaby.node.glif.io/rpc/v1 (for new API v1 - see [API README](https://github.com/filecoin-project/lotus/blob/422f66776fa07827f2cfa9d2f8142ef29dcd2a95/api/README.md))
  - web socket endpoint: wss://wss.wallaby.node.glif.io/apigw/lotus/rpc/v0
- **JSON RPC API - Private Endpoints**:
  - Protected by JWT authorization. Ping @glif-nodes-team in wallaby slack channels to obtain the token.
  - https://wallaby.dev.node.glif.io/archive/lotus/rpc/v0
  - https://wallaby.dev.node.glif.io/archive/lotus/rpc/v1
- **Wallaby SPs auto-accepting storage deals:**
  - 
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
  - Use the [faucet](https://wallaby.filtest.network/#faucet) to draw funds to your f4 (0x style addresses are translated automatically to f4's in the backend) or alternatively use `lotus send` to transfer funds to the f4 address.
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
