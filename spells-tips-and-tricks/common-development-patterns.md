# Common Development Patterns

### Deploying an Anchor Program

These are the best steps for deploying an anchor program for the first time:

1. Ensure you confirm what cluster you are deploying to in **Anchor.toml**
2. Ensure you confirm what wallet you are using to deploy the program in **Anchor.toml**
3. Run `anchor build`
4. Run `solana-keygen pubkey target/deploy/<program-keypair>.json`
5. Copy this PubKey to:
   * **lib.rs** `declare_id!(<PubkKey>);`
   * **Anchor.toml**
6. Run `anchor build`
7. Run `anchor deploy`
   * In our experience you must have \~double the required SOL in your account to successfully deploy the program for the first time
