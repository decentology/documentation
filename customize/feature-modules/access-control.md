---
description: >-
  Once a smart contract has been deployed, you cannot change your code. Access
  Control Blocks give you granular control over who can manage your contracts
  and control their operation.
---

# 🔓 Access Control

## Contract Run State

**Ability to pause operation of your smart contract.**

| Type | **Function**                     | **What it does**                              |
| ---- | -------------------------------- | --------------------------------------------- |
| GET  | **Is Contract Run State Active** | Checks if the contract run state is active    |
| POST | **Set Contract Run State**       | Sets contract run state to active or inactive |

## **Administrator Roles**

**Define accounts that can perform certain admin functions. This allows users to add different accounts for administrative purposes.**

Every blockchain represents a user as an account. Every account has an address and typically a given account will have a public key and a private key (though some require multiple).

| Type | **Function**                   | **What it does**                                   |
| ---- | ------------------------------ | -------------------------------------------------- |
| GET  | **Is Contract Admin**          | Checks if given address is a contract admin        |
| POST | **Add Contract Admin**         | Adds given address as contract admin               |
| POST | **Remove Contract Admin**      | Removes given address from contract admin          |
| POST | **Remove Last Contract Admin** | Removes last remaining admin address from contract |

{% hint style="danger" %}
**Remove Last Contract Admin** will remove the last remaining administrator on the contract. Any functions that require requireContractAdmin() will fail, effectively making this a fully decentralized contract. This action is irreversible.
{% endhint %}

## Contract Access

**Control which external contracts can interact with your contract.**

| **Type** | **Function**               | **What it does**                                                              |
| -------- | -------------------------- | ----------------------------------------------------------------------------- |
| GET      | **Is Contract Authorized** | Checks if a contract is authorized                                            |
| POST     | **Authorize Contract**     | Authorizes a contract, functions must check using requireContractAuthorized() |
| POST     | **Deauthorize Contract**   |  Deauthorizes a contract                                                      |

{% hint style="danger" %}
**You will want to restrict some of your state contract functions so only authorized contracts can call them. **This can be achieved in four steps:

**1) Include the "Access Control: Contract Access" feature block when creating your project. **This adds all the functionality to manage white-listing of external contracts in your state contract.

**2) Add the "requireContractAuthorized" function modifiers to those state contract functions that should be restricted.**

**3) Deploy the contract that will be calling into the state contract (like this one, for example).**

**4) Call the "authorizeContract()" function in the state contract with the deployed address of the calling contract. **This adds the calling contract to a white-list. Thereafter, any calls to any function in the state contract that use the "requireContractAuthorized" function modifier will succeed only if the calling contract (or any caller for that matter) is white-listed.
{% endhint %}
