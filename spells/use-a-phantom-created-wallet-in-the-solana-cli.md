# Use a Phantom created wallet in the Solana-CLI

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
