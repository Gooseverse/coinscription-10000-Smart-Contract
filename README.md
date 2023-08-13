# coinscription-10000-Smart-Contract

The Coinscription Smart Contract is designed to facilitate the minting and collection of a large number of Ethscriptions while ensuring a minimum fee is paid per minting transaction. Once a specified number of minting transactions are reached, the contract will collect the metadata of each Ethscription and transfer ownership to the original minter.

## Overview

The Coinscription Smart Contract consists of the following main functionalities:

1. Mint Ethscriptions: Authorized minters can use this function to mint Ethscriptions by providing JSON metadata and paying a minimum deposit of 0.01 ETH.

2. Collect Ethscriptions: Once a certain number of minting transactions are reached, the contract owner can initiate the collection process. This involves transferring ownership of Ethscriptions to the original minters and collecting metadata.

## Usage

### Prerequisites

- Solidity compiler (version 0.8.0 or higher)
- Ethereum development environment (e.g., Remix, Truffle)
- Ethereum wallet for deploying and interacting with the contract

### Deployment

1. Compile the `CoinscriptionContract.sol` Solidity file using your preferred development environment.

2. Deploy the compiled contract to the Ethereum blockchain using your chosen deployment tool (e.g., Remix, Truffle, Hardhat).

### Functions

#### `addMinter(address minter)`

Allows the contract owner to add authorized minters.

#### `mintEthscription(string metadata)`

Authorized minters can use this function to mint Ethscriptions by providing JSON metadata and paying a minimum deposit of 0.01 ETH.

#### `collectEthscriptions()`

The contract owner can use this function to collect Ethscriptions once a certain number of minting transactions are reached. The metadata is collected, and ownership is transferred to the original minters.

## Security Considerations

- The contract has implemented access control mechanisms to ensure that only authorized parties can interact with specific functions.
- The contract uses the nonReentrant modifier to prevent reentrancy attacks.
- Users are responsible for covering gas fees for their transactions.
- It's important to thoroughly test and audit the contract to ensure its security and functionality before deploying it on the mainnet.

## Disclaimer

This smart contract is provided as an example and should not be considered production-ready without thorough testing and auditing. Use it at your own risk.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
