# Common Errors

### Anchor

#### Program Errors

When Anchor throws a Custom Program Error it will look something like this

```
Error processing Instruction 0: custom program error: 0x<some hex here>
```

Here are some common error codes and their meanings:

**0xa7** Error: 167: The given account is not owned by the executing program

**0xa2** Error: 162: 8 byte discriminator did not match what was expected

**0x0** Error: An account with that address already exists

### Solana JavaScript API

#### SPL Tokens

When dealing with SPL Tokens (Fungible or Non-Fungible) don't forget to import the npm bindings for the token program&#x20;

```javascript
npm i @solana/spl-token
```

These are separate imports from @solana/web3.js









