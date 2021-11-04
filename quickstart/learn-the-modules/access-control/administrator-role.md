---
description: Define accounts that can perform admin functions.
---

# Administrator Role

## **Definition**

**Smart contracts** often include functions that should only be available to a select group of accounts. Typically, these are privileged functions that are used to manage or configure the smart contract. The Administrator Role adds the ability to manage a list of administrators. It also provides sample code to demonstrate how any smart contract function can check if an account belongs to the administrator role before executing privileged code.

### **Dependencies**

* None

## **Benefit**

**The Administrator Role module** is useful in any scenario where it’s necessary to define and manage a list of accounts that have access to privileged capabilities in the smart contract.

## **When to Use?**

**We recommend** including the Administrator Role module in all smart contracts that have features that should not be available to all accounts such as configuration or management of the contract.\
****
