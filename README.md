> **IMPORTANT:** *This repo is a work in progress, and contracts have not been audited. Use at your own risk.*

<br/>
 
<br/>


# RWAs
 
# The Methodology

We can tokenize real world assets by combining any of the following traits:
- Asset location: 
  - On or Off Chain Asset Represented 
  - Nomenclature: [`AOn`, `AOff`] 
    - Note: By using an on-chain asset, it could be considered no longer "real world".
- Collateral location: 
  - On or Off-Chain Collateral 
  - Nomenclature: [`COn`, `COff`] 
- Backing type:
  - Direct backing or Indirect (synthetic)
  - Nomenclature: [`DB`, `SB`]

So since we have 3 categories each with 2 options, we have 8 different types of RWAs. 
### Examples that would make sense 
- Synthetic Off-Chain Asset Representation with Off-Chain Collateral
  - This would be like a synthetic index fund share, but backed by shares of different stocks.
</details>


<br/>
<p align="center">
<img src="./img/tokenized-assets.svg" width="700" alt="tokenized-assets">
</p>
<br/>
 
## dTSLA.sol

### V1
1. Only the owner can mint `dTSLA`
2. Anyone can redeem `dTSLA` for `USDC` or "the stablecoin" of choice.
  - Chainlink functions will kick off a `TSLA` sell for USDC, and then send it to the contract
3. The user will have to then call `finishRedeem` to get their `USDC`.
   
 
 