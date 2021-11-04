# Access Control

**Collection of feature modules** that give you granular control over who can manage your contracts and control their operation. Any code submitted to a blockchain is unalterable, therefore once a smart contract has been deployed, a developer can’t go back and implement changes. The architectural solutions in this category provide the opportunity to update a smart contract even after development.

## **Definition**

**The Access Control module** gives you granular control over who can manage your contracts and control their operation.

* ****[**Contract Run State**](contract-run-state.md) gives you ability to pause operation of your smart contract
* [**Administrator Role**](administrator-role.md) allows you to define accounts (addresses) that can perform certain administrative functions
* [**Contract Access**](contract-access.md) lets you control which external contracts can interact with your contract

## **Example**

A developer needs to deploy an early iteration of a dapp to the mainnet. They are aware of the limitations on upgradability, but they decide to go around Ethereum’s immutability by using multi-contract architecture. To make sure that they are able to allow upgraded contracts calling into the main one, and restrict unauthorized access, they’ll need to use the Contract Access module.

**In the case of a bug in a smart contract:**

* **Contract Run State** allows an administrator to pause the smart contract to avoid various losses
* **Administrator Role** defines who has the ability to perform functions such as pausing the contract
* **Contract Access** allows an administrator to control which external contracts can interact with your contract, safeguarding it from unauthorised access

## **Benefits**

**By making smart architectural choices**, developers can avoid the pitfalls of blockchain and smart contract immutability while still reaping the network’s benefits.

The Access Control module allows:

* **Upgradability** of a decentralized application even after deployment to mainnet
* **Enhanced security** in the case of bugs

