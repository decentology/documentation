---
description: Control which external contracts can interact with your contract.
---

# Contract Access

## Definition

**Smart contracts** deployed to most blockchains are immutable. But what if the smart contract has a bug that is discovered after deployment? Disabling the smart contract and migrating data to a new smart contract instance can be prohibitively expensive. The solution is to partition your contract so the “state” or data and “application” or business logic are in separate contracts. This is the default architecture in DappStarter. The “DappState” contract contains included modules and their data, and the “Dapp” contract should contain your custom application code.\


This is where the Contract Access module comes into the picture. By including this module, you can restrict external contracts that call into your contract with a white-list of contract addresses. For instance, let’s say your initial DappState contract is S, and your initial Dapp contract is A. You can add A as an authorized contract initially. Later, if you want to deprecate A and introduce a revised Dapp contract B, you can remove A from the Contract Access authorized contracts list and replace it with B.

### Dependencies

* ****[**Administrator Role:**](administrator-role.md) The Administrator Role module is automatically included so you can define the accounts that are authorized to manage the list of authorized external contracts. By default, the owner of the smart contract is the only authorized account.

## Benefit

**The Contract Access module** makes your smart contract more secure by restricting the addresses of external contracts that can make calls to functions in your contract.

## When to Use?

**We recommend** using the Contract Access module when you want to restrict which external smart contracts can interact with your contract.\
