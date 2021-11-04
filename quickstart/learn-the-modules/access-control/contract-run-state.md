---
description: The ability to stop/start operation of your smart contract.
---

# Contract Run State

## **Definition**

**Smart contracts** are autonomous by design, i.e. once deployed, they’re able to run without any further input. However, the desired degree of autonomy will naturally vary based on the use case. In some scenarios, it may be beneficial to be able to stop/start a smart contract much like a developer would do with a web, API, or database server. The Contract Run State adds the ability for authorized accounts to stop and start the operation on demand.

### **Dependencies**

* ****[**Administrator Role:**](administrator-role.md) The Administrator Role module is automatically included with Contract Run State, because the developer needs to define the accounts that are authorized to stop and start the smart contract. By default, the owner of the smart contract is the only authorized account.

## **Benefit**

The Contract Run State module:

* **helps prevent** undesirable events from happening within your smart contract
  * e.g., if there is a vulnerability discovered in a smart contract, the developer may want to stop it from running until they have developed a mitigation plan
* **enables** the contract to remain autonomous, but the the on/off switch gives the developer a certain degree of control over its operation

## **When to Use?**

**We recommend** including the Contract Run State module in EVERY smart contract unless the business requirement calls for full autonomy.\
