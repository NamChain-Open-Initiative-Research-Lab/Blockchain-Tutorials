# NamChain - Open Initiative Research Lab ![](https://img.shields.io/badge/Project-Nam-ff69b4.svg) ![](https://img.shields.io/badge/madeby-Ramaguru-blue.svg)

<p align="center">
<img src="https://1.bp.blogspot.com/-0SArWfduw68/XkxV8EmBBcI/AAAAAAAAABw/h9aWSWbm0J4kilgn3xddzQ3PdoP-e3RZgCLcBGAsYHQ/s1600/SAVE_20200127_132431.jpg" width="200" align="center">
</p>  

## Ethereum Blockchain Tutorials

This repository is dedicated to Ethereum Blockchain. Here you can find examples related to Smart Contract and DApps.

## Prerequisite
- Knowledge on 
    - HTML
    - CSS
    - JavaScript
    
 - Install
    - Metamask Browser Extension
    - [Test Ethers from Faucet](https://faucet.metamask.io/)
    - [IPFS Companion Browser Extension](https://ipfs.io/)
    - [IPFS Desktop](https://ipfs.io/)
    
 ## Tutorial Topics
    - Ethereum Blockchain
    - Solidity Programming Language
    - Metamask and Faucet
    - Web3.js
    - Interplanetary File System (IPFS)
    - Tokens (ERC-20, ERC-721, ERC-1155)
    - Identity Management Standards (ERC-725 and ERC-735)
      
## Ethereum Blockchain

<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6f/Ethereum-icon-purple.svg/330px-Ethereum-icon-purple.svg.png" width="200" align="center">
</p>  

Ethereum is a second generation Blockchain Technology which is widely referred to as *World Computer*. The native cryptocurrency of the Ethereum Blockchain is called **"Ether (ETH)"**. Ethereum also provides the users the programming capability through its Smart Contract Programming. **Distributed Application (DApps)** can be developed using the smart contracts which is deployed and runs on the Ethereum Blockchain. 

Ethereum Blockchain uses **Ethereum Virtual Machine (EVM)** to execute the transactions. Ethereum uses memory-based Proof of Work (PoW) consensus algorithm. It also offers multiple testnets (Ropsten, Goerli, Kovan, Rinkeby) and dedicated private blockchain (Ganache) support for the development of smart contracts. 

## Solidity Programming

**Solidity** is the dedicated programming language for development of Smart Contracts on Ethereum Blockchain. Solidity is similar to Object Oriented Programming Language. ***Contract*** is the main component in the solidity programming which is similar to ***Class*** in Java. Like, Java, the solidity program on compilation is converted into bytecode for execution in EVM. 

To program Solidity Smart Contracts, Ethereum provides its own online IDE called [Remix](https://remix.ethereum.org/)

## Metamask and Faucet

**Metamask** is a Browser Extension, is a tool which acts as a bridge for communication between the traditional browser to the blockchain (Distributed Web). Web3.js is used in the User Interface Component to enable communication with the Blockchain via Metamask. More on Metamask is [here](https://namchain.blogspot.com/p/metamask.html).

<p align="center">
<img src="https://metamask.io/images/mm-logo.svg" width="200" align="center">
</p>  

**Faucet** is a developer support system which provides the Ether for development and testing purposes to our wallet address.

## Web3.js

**Web3.js** is a collection of javascript libraries which enables communication with local or remote Ethereum using HTTP or RPC communication.

## IPFS

**Interplanetary File System** is a protocol and a peer-to-peer file sharing and storage distributed network. IPFS is a content-addressed system, where a file is identified by its hash. IPFS complements the Blockchain for storage. 

## Tokens 
    - ERC-20 - Fungible Tokens
    - ERC-721 - Non-Fungible Tokens (NFT)
    - ERC-1155 - Multi-Token 

## Examples

- MetaMask Connection
   - [DApp](Simple%20DApps/NamChain_Tutorials_Metamask_Connection.html)

- Storage and Retrieval
    - [DApp](Simple%20DApps/NamChain_Tutorials_Storage_Smart_Contract.html)
    - Storage.sol - Refer remix.ethereum.org
        - [Contract Link](https://ropsten.etherscan.io/address/0xb3c65fc8a5b71eb48a8c35c52232d989ca6a8205)

- Money Transfer
    - [Sender.sol](https://ipfs.io/ipfs/Qmf3Wd2jvt15TVycq65h7JobHuqoyzQ9E4MZJLNtshzbZR)
        - [Contract Link](https://ropsten.etherscan.io/address/0xc7fb9a8410e0b228abaa4fccd63a8b22164f00bf)
    - [Receiver.sol](https://ipfs.io/ipfs/QmaXQ5WFn12q7cXCRQyVV3XuBpkhZuPWHB66BLcgX7LVtY)
        - [Contract Link](https://ropsten.etherscan.io/address/0xf5dc36a0eeec4909f3e09cfdc9b29e2343a1c73c)
  
 - Registry
    - [Registry.sol](https://ipfs.io/ipfs/Qmd73HXiwnhCsGZ7uqoT1QaUeikSg6j4A6fUdb5KGAKyMT)
        - [Contract Link](https://ropsten.etherscan.io/address/0x13248d484eecb610cad3e9e03f8e7b8d477193b2)
    - [Registry_Project.sol](https://ipfs.io/ipfs/QmPyLAAi5VXx7CmBjJQPojkshMNkbeRw1YAtUMQwCuUTid)
        - [Contract Link](https://ropsten.etherscan.io/address/0xce2b4087cec369d9ec2dfdece9296b36134ff4bb)
        
  - Events and Notification
    - [DApp](Simple%20DApps/NamChain_Tutorials_Events.html)
    - [Events.sol](https://ipfs.io/ipfs/QmTFCP8uyL4UFqUQqH9PsQYJhpxtLsHoA6pP5ZQMyAkaCp)
        - [Contract Link](https://ropsten.etherscan.io/address/0x7d35606eacac8652f2a38c5a52128100e6545871)
    - [NotificationReceiver.sol](https://ipfs.io/ipfs/QmbiMjH9UZi8yYoDG5J5V8Vz7CKUD9d5K4rCUR8H92Z1Q4)
        - [Contract Link](https://ropsten.etherscan.io/address/0xe266c99a858aef94edb852709d79bf04771dc74f)
  
  - Access Modifiers
    - [Access.sol](https://ipfs.io/ipfs/QmXUnabQ5YkSrCu613xmwrpSC5MxSuPCgVdZXNb9JFAACz)
        - [Contract Link](https://ropsten.etherscan.io/address/0xef24ce272e971b7771c7ed5f16001295d5570932)
        
  - ERC721 NFT - RAMCoin     
    - [DApp](Simple%20DApps/NamChain_Tutorials_RAM_ERC721_Token.html) 
    - [MyERC721Token.sol](https://ipfs.io/ipfs/QmaCKsKDWMK8nmip51YCBgaUakU6zErwBnM6i8NdgPhdna)
        - [Contract Link](https://ropsten.etherscan.io/address/0xecff6e3fdf43146ae8e5a093a82b922777218807)
        - [NFT Token Tracker](https://ropsten.etherscan.io/address/0xecff6e3fdf43146ae8e5a093a82b922777218807)

- One Click DApp 
    One Click DApp is a 3rd party service which generates a UI which can be accessed using a public link.
    - [Store and Retrieve](https://oneclickdapp.com/learn-unit/)

- DApp Hero 
    DApp Hero is a 3rd party service which generates HTML page / Website based on your Smart Contract, enabling the developer in quick       DApp creation.
    - [Store and Retrieve](Simple%20DApps/DAppHero_Example.html)

# License

[MIT](https://github.com/ramagururadhakrishnan/NamChain/blob/master/MIT)
