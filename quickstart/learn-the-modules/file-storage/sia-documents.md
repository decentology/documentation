---
description: >-
  Store data files on the Sia platform and reference them with hash pointers in
  the smart contract.
---

# Sia Documents

## Definition

[**Sia**](https://sia.tech) is a decentralized file storage system that relies on a network of volunteer-hosted, peer-to-peer nodes to provide distributed file storage capabilities. Sia and similar decentralized storage systems address the issue of prohibitively high blockchain storage costs.&#x20;

A typical smart contract design pattern is to store the unique hash returned by Sia for any uploaded data files (JSON, PDF, media, text). The files are immutable and remain available as long as at least a single Sia node has them hosted. Files stored on Sia are “content addressable” which means that once the hash for a file is known, it can be retrieved from any Sia “gateway” (the portion of the Sia node that enables web access to files). The front-end UI for the smart contract (if any) can fetch and display the file content for users from any Sia gateway with just the hash stored in the smart contract.

The Sia Documents module fully implements the above design pattern and makes it easy for you to extend your smart contract with any type of data. In this module the data file is called a “document” representing an arbitrary file in any format.

**Caution:** Files stored on Sia are public. If you want a file to be private, you should encrypt it before storing it on Sia.

To learn more, see [Sia API documentation](https://sia.tech/docs/) and [Sia Support Center](https://support.sia.tech)

### Parameters

* **Single-document Upload:** Restricts the web uploader user interface to allowing only a single file to be uploaded for a transaction.
* **Multiple-document Upload:** Enables the web uploader user interface to allow multiple files to be uploaded for a transaction.

Note: The web uploader restricts the upload size to 10MB. This is an arbitrary number and you can change it in the module source code.

### Dependencies

* None

## Benefit

**Smart contract data storage** is famously expensive due to the nature of decentralized computation. It isn’t unusual to encounter blockchains where it might cost upwards of $500,000 to store 1 Gb of data, compared to cloud storage which usually offers a cost of a couple cents per 1 Gb of data. Using the Sia Documents module, you can extend your smart contracts to use any data files stored on Sia thus avoiding the storage costs.&#x20;

## When to Use?

**We recommend** using the Sia Documents module when your smart contract needs to manage data beyond what one might store in a typical data object. Candidates include JSON, PDF, media and archive files.\
