# burn-to-claim-formal-verification
## Implementation of paper [Formal Verification of the Burn-to-Claim Protocol] (https://www.researchgate.net/publication/361388545_Formal_Verification_of_the_Burn-to-Claim_Protocol_for_Blockchain_Interoperability) for Blockchain Interoperability based on PAT models. 


At the very high level, we aim to construct a model that consists of a scenario where a user wishes to transfer an asset from a blockchain network to another blockchain network. The  [Burn-to-Claim](https://www.researchgate.net/publication/354880774_Burn-to-Claim_An_asset_transfer_protocol_for_blockchain_interoperability/). protocol executes the transfer process so that the asset is being destroyed (removed) from one blockchain network and re-created on the other blockchain network. The networks involved in this process are source networks from where the asset is removed and destination networks to where the asset is moved. The transfer process consists of two parts: first, the source network generates a self-verifiable transfer-proof, and second, the destination network regenerates the asset upon verifying the proof.

![This is an image](./protocol%20overview.PNG)

Above figure illustrates a brief overview of the transfer process with exitTransaction function that generates the transferProof and entryTransaction function} to verify the proof and regenerate the asset, demonstrating a cross-chain protocol workflow. The diagram represents the process and workflow involved in transferring value from one network to another.


We present two models in this paper. The first is a [model for cross-blockchain interactions](./interaction%20model/) a light version of value transfer process using the Burn-to-Claim protocol where we omitted the complexity of block creation and mining reward. The second is a [model for blockchain internal operations](./internal%20operation%20model/) that includes the block creation and mining aspects to demonstrate blockchain mechanism. In the second model, we use the concept of merge mining, where the network miners will mine in both networks.