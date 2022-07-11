# 💾 File Storage

Solana NFTs rely on two pieces of off-chain information

1. The underlying asset (image, gif, video)
2. The off-chain metadata

There are many ways to store this data. The most common are:

[Arweave](https://www.arweave.org/)

* Here's great [example code](https://solanacookbook.com/references/nfts.html#upload-to-arweave) for uploading to Arweave

[IPFS](https://ipfs.io/)

* Here's a great [example](https://flyingzumwalt.gitbooks.io/decentralized-web-primer/content/files-on-ipfs/lessons/add-and-retrieve-file-content.html) for uploading to IPFS

[AWS S3](https://aws.amazon.com/s3/)

{% hint style="info" %}
AWS S3 is not considered a fully-decentralized storage option and data can be mutated or deleted directly by the owner the AWS account where the data is stored
{% endhint %}
