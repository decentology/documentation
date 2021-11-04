---
description: >-
  Create a fungible token using the ERC-20 industry standard for tracking value
  within an Ethereum-based smart contract.
---

# Custom Fungible Token

## Definition

**Smart contracts** often need a store of value in addition to the native cryptocurrency of the blockchain platform on which they are built. “Tokens” implemented in smart contract code enable such storage of value. However, such tokens are siloed unless they conform to a specification that enables users to trade such tokens. The most popular standard for smart contract tokens is [ERC-20](https://eips.ethereum.org/EIPS/eip-20). The Custom Token module implements the ERC-20 specification and makes it easy to add fungible token capabilities to your smart contract.

### Parameters

* **Token Name:** An arbitrary name for the token.
* **Token Symbol:** A symbol to identify your token for various purposes, e.g. exchanges, wallets. By convention, this is 3-5 uppercase letters (“ETH”, “QZR”)
* **Decimals:** A number of decimal places your token will be divisible to. Unlike fiat currencies, smart contract-based tokens and blockchain cryptocurrencies have the unique ability to be sent in very small quantities. The number of decimal places you choose determines how small the minimum trading amount of the token will be.
  * Recommended: 18 decimals
* **Initial Supply:** A number of tokens that should initially exist; this can be 0 or any other number. A token in a smart contract is a unit representing a store of value. Your smart contract code ultimately determines when that number (“the supply”) is increased (called “minting”) or decreased (called “burning”).&#x20;
  * Recommended: Set this to 1 million if unsure —this can easily be changed in the code later.&#x20;

### Dependencies

* None

## Benefits

* **Track** value of digital assets (e.g., users can receive, send, and earn tokens)
* **Implement **token-related features, e.g. rewards, staking, or voting based on token scarcity
* **Leverage** the established ERC-20 standard including token interoperability, exchange services, and wallet integrations

## Example

**Company A** wants to build a loyalty system to reward customers for their purchases at the store. They use the Custom Token module to create an ERC-20 token and distribute their token to customers for each transaction made at the store.

**An example token would have the following attributes:**

**Token Name:** Buy With Us

**Token Symbol:** BWU

**Decimals**: 18

**Initial Supply:** 1,000,000

## When to Use?

**We recommend** using the Custom Token module when you need a mechanism for users to earn value and trade or redeem it with the smart contract for benefits or privileges, or with other users for entertainment or virtual goods.\
