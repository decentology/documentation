---
description: >-
  Data storage on blockchains is expensive. That’s why all decentralized
  applications have to decide what to store “on-chain” (on the blockchain) and
  “off-chain” (on another data storage solution).
---

# File Storage

## Definition

****[**IPFS Documents** ](ipfs-documents.md)is a peer-2-peer data, decentralized storage and access system.

* Single-document Upload
  * Smart contract stores one hash that points to a document on your file storage provider of choice.
* Multiple-document Upload
  * Smart contract stores several hashes that point to specific documents on your file storage provider of choice.
* Multiple-document Upload with Folder
  * Smart contract stores one hash that points to a folder containing multiple documents.

[**Sia Documents**](sia-documents.md) is a data storage platform combining a peer-to-peer network with blockchain technology.&#x20;

* Single-document Upload
  * Smart contract stores one hash that points to a document on your file storage provider of choice.
* Multiple-document Upload
  * Smart contract stores several hashes that point to specific documents on your file storage provider of choice.

## Why?

**Coming to the realization** that not all data storage can sensibly be done on the blockchain (except for rudimentary dapps), developers need to decide which data absolutely MUST be stored on-chain (such as token ownership), and which can be delegated to off-chain services.

## Example

**A publisher** wants to create unique NFTs to represent collectible versions of famous books. The NFT representing a given book is stored on-chain, but the content (written text) of that book is stored on IPFS off-chain using the file storage module.

## Benefits

* **Solve** the on-chain/off-chain dilemma without relying on a single-point-of-failure cloud computing platform
* **Leverage **the secure and robust nature of Ethereum data storage in the most important parts of the decentralized application
* **Maintain** decentralization by using a p2p network for data stored off-chain
