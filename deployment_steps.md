# Deployment steps:

1. Use a branch @jennijuju will prepare based on M2 branch at https://github.com/filecoin-project/lotus/tree/experimental/fvm-m2
2. Add `build/params_wallaby.go`
3. Create PR to Lotus
4. Wait 24 hours for any community requests for changes
5. Deploy the testnet
6. Ask the Lotus team to create a tag
7. Update this `filecoin-project/testnet-wallaby` repo's [README](README.md) with exact commit/tag used
8. Notify testnet RPC endpoint providers and Filscan
9. Update FVM early builders 
