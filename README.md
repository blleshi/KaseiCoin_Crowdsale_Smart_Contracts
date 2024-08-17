# KaseiCoin Crowdsale Smart Contracts

## Overview

This project involves creating a new cryptocurrency named **KaseiCoin** (where "Kasei" means "Mars" in Japanese), which will be a fungible ERC-20 token. The token will be minted via a crowdsale, allowing users to convert their money to KaseiCoin as part of a larger initiative to facilitate transactions for those moving to Mars.

### What's Created:

1. **KaseiCoin Token Contract**: An ERC-20 compliant fungible token.
2. **KaseiCoin Crowdsale Contract**: A smart contract managing the entire crowdsale process, allowing users to send ether in exchange for KaseiCoin tokens.
3. **KaseiCoin Deployer Contract**: A contract to deploy both the token and crowdsale contracts.
4. **Evaluation Evidence**: A set of screenshots or a video demonstrating the successful deployment and functionality of the contracts.


## Instructions

### 1. Create the KaseiCoin Token Contract

1. Import the provided `KaseiCoin.sol` starter file into the Remix IDE.
2. Import the following contracts from the OpenZeppelin library:
   - `ERC20`
   - `ERC20Detailed`
   - `ERC20Mintable`
3. Define a contract named `KaseiCoin` that inherits from the three imported contracts.
4. Add a constructor with parameters: `name`, `symbol`, and `initial_supply`. Call the `ERC20Detailed` constructor with `name`, `symbol`, and `18` (for decimals).
5. Compile the contract using version 0.5.5 of the compiler.
6. Debug any errors, if present.
7. Take a screenshot of the successful compilation and add it to the Evaluation Evidence section.

### 2. Create the KaseiCoin Crowdsale Contract

1. Import the provided `KaseiCoinCrowdsale.sol` starter code into the Remix IDE.
2. Have the contract inherit from the following OpenZeppelin contracts:
   - `Crowdsale`
   - `MintedCrowdsale`
3. In the constructor, provide parameters for the crowdsale features: `rate`, `wallet`, and `token`. Configure these as needed.
4. Compile the contract using version 0.5.5 of the compiler.
5. Debug any errors, if present.
6. Take a screenshot of the successful compilation and add it to the Evaluation Evidence section.

### 3. Create the KaseiCoin Deployer Contract

1. Uncomment the `KaseiCoinCrowdsaleDeployer` contract in the provided `KaseiCoinCrowdsale.sol` starter code.
2. Add variables to store the addresses of the KaseiCoin and KaseiCoinCrowdsale contracts.
   - `address public kasei_token_address;`
   - `address public kasei_crowdsale_address;`
3. In the constructor, add the parameters `name`, `symbol`, and `wallet`.
4. Complete the constructor by:
   - Creating the KaseiCoin token with an initial supply of 0.
   - Storing the token's address in `kasei_token_address`.
   - Creating the KaseiCoinCrowdsale contract with appropriate parameters.
   - Storing the crowdsale contract's address in `kasei_crowdsale_address`.
   - Setting the KaseiCoinCrowdsale contract as a minter and renouncing the minter role of the deployer.
5. Compile the contract using version 0.5.5 of the compiler.
6. Debug any errors, if present.
7. Take a screenshot of the successful compilation and add it to the Evaluation Evidence section.

### 4. Deploy the Crowdsale to a Local Blockchain

1. Deploy the crowdsale to a local blockchain using Remix, MetaMask, and Ganache.
2. Test the crowdsale functionality by:
   - Using test accounts to buy tokens.
   - Checking balances to ensure correct token distribution.
3. Review the total supply of minted tokens and the amount of wei raised by the crowdsale.
4. Record a short video or take screenshots that illustrate these steps as evidence.
   - If using screenshots, add them to the Evaluation Evidence section.
   - If using a video, upload it to a hosting platform and include the link in the README.md file.

### 5. (Optional) Extend the Crowdsale Contract Using OpenZeppelin

1. Import the following contracts from OpenZeppelin:
   - `CappedCrowdsale`
   - `TimedCrowdsale`
   - `RefundablePostDeliveryCrowdsale`
2. Modify the `KaseiCoinCrowdsale` contract to inherit from these contracts.
3. Update the constructor to include parameters for `goal`, `open`, and `close` times.
4. Adjust the `KaseiCoinCrowdsaleDeployer` contract to handle the new crowdsale contract.
5. Compile, test, and ensure that the updated contract meets the desired functionality.
6. Record the deployment and testing steps as evidence.

## Evaluation Evidence

Place your screenshots or video here to demonstrate the successful compilation, deployment, and functionality of the KaseiCoin smart contracts.

- **KaseiCoin Token Contract Compilation**: ![KaseiCoin Token Compilation](screenshot1.png)
- **KaseiCoin Crowdsale Contract Compilation**: ![KaseiCoin Crowdsale Compilation](screenshot2.png)
- **KaseiCoin Deployer Contract Compilation**: ![KaseiCoin Deployer Compilation](screenshot3.png)
- **Crowdsale Deployment Evidence**: [Crowdsale Deployment Video](https://www.example.com)

