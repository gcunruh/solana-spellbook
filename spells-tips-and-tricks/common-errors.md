# Common Errors

### Wallets

If you need to use a Phantom created wallet in the Solana-CLI:

1. Export Private Key from Phantom using Settings->Show Private Key
2.  Using JS, run the following:

    ```javascript
    const bs58 = require('bs58');
    const fs = require('fs');
    b = bs58.decode(<PRIVATE KEY FROM PHANTOM>);
    j = new Uint8Array(b.buffer, b.byteOffset, b.byteLength / Uint8Array.BYTES_PER_ELEMENT);
    fs.writeFileSync('key.json', `[${j}]`);
    ```

This Private Key can now be used in the Solana CLI using the --keypair flag

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

These are separate from @solana/web3.js









