# நம்Chain® Open Initiative Research Lab ![](https://img.shields.io/badge/Project-Nam-ff69b4.svg) ![](https://img.shields.io/badge/madeby-Ramaguru-blue.svg)

## Welcome to Corda Tutorials

A Repository dedicated to Corda Tutorials.

## Prerequisite
- Knowledge on 
    - Blockchain Basics
    - Bitcoin Blockchain Basics
    
## Tutorial Topics
  - [Corda Blockchain Overview](corda-overview)
  - [Corda Architecture](corda-architecture)
  - [CorDApps](cordapps)
  - [Examples](examples)
          
## Corda Overview
<p align="center">
<img src="https://camo.githubusercontent.com/382022967fd064ec30f44fe98950616b59cec5f45f1e9e6597df61f0965b17c0/68747470733a2f2f7777772e636f7264612e6e65742f77702d636f6e74656e742f7468656d65732f636f7264612f6173736574732f696d616765732f637264612d6c6f676f2d6269672e737667" width="200" align="center">
</p>  

Corda is a distributed open source peer-to-peer network developed based on JVM written in Kotlin.

### Features of Corda
   - Scalability through Notary Services
   - Privacy through parital visibility of data with no global ledger
   - Transaction Finality 
   - Support for Multiple Consensus
   - Productivity
   - Integration
    
## Corda Architecture
   - Certificate Authority
        - Root CA 
        - Doorman CA
        - Network CA
   - Identity (X.509 Certificate)
        - Well Known Identity
        - Confidential Identity
   - Network
        - Network Map
        - Notary Service
            - Verifying 
            - Non-Verifying 
        - Oracle Service
   - Nodes
        - Vault
        - Persistance Layer
        - Network/RPC Interface
        - Service Hub
        - CorDapp Interface
        - Storage Service
            - Transactions
            - Attachments
            - Flow Checkpoint
   - Flow Framework
        - Inlined Flows
        - Initiating Flows
   - Ledger
   - States
   - Transactions
        - Notary 
        - General
        - Components
            - Commands
            - List of Signers
            - Attachments
            - Time Window
   - Consensus 
        - Validity 
        - Uniqueness
   - Contracts (written in JVM Languages like Java or Kotlin)
   - CorDapp

## CorDApps

## Examples


# License

MIT
