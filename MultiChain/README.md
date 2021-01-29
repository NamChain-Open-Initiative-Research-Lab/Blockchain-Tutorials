# நம்Chain - Open Initiative Research Lab ![](https://img.shields.io/badge/Project-Nam-ff69b4.svg) ![](https://img.shields.io/badge/madeby-Ramaguru-blue.svg)

<p align="center">
<img src="https://1.bp.blogspot.com/-0SArWfduw68/XkxV8EmBBcI/AAAAAAAAABw/h9aWSWbm0J4kilgn3xddzQ3PdoP-e3RZgCLcBGAsYHQ/s1600/SAVE_20200127_132431.jpg" width="200" align="center">
</p>  

## MultiChain Tutorials

A Repository dedicated to MultiChain Tutorials.

## Prerequisite
- Knowledge on 
    - Blockchain Basics
    
 - Install
    - MultiChain Client
    
## Tutorial Topics
  - [MultiChain Overview](#multiChain-overview)

          
## MultiChain Overview

<p align="center">
<img src="https://www.multichain.com/assets/multichain-temp-logo-228x48.png" width="400" align="center">
</p>  

<b>MultiChain</b> an off-the-shelf platform based on bitcoin (fork of Bitcoin Core), for the creation and deployment of private blockchains, either within or between organizations. MultiChain aims to overcome a key obstacle to the deployment of blockchain technology in the institutional financial sector, by providing the privacy and control required in an easy-to-use package. It uses bitcoin’s protocol, transaction and blockchain architecture, with changes only to the handshaking process when two nodes initially connect. All other features are implemented using metadata and modifications to the validation rules for transactions and blocks. 

MultiChain supports configuring multiple blockchains in a system at same time and can also serves as a Multicurrency platforms.

## MultiChain Configuration

MultiChain allows the user to set the parameters in a configuration file. There are multiple parameters based on Consensus, mining, etc. Some parameters include
 - The chain’s protocol, i.e. private blockchain or pure bitcoin­like.
 - Block Interval, e.g. 1 minute.
 - Active permission types, e.g. anyone can connect, only some can send/receive. 
 - Mining diversity (private blockchains only) i.e., 0 ≤ mining diversity ≤ 1
 - Level of consensus required for creating/removing administrators and miners, and the duration of the setup phase in which this is not enforced (private blockchains only).
 - Mining rewards, e.g. 50 native currency units per block, halving every 210,000 blocks.
 - IP ports for peer-to-peer connections and the JSON-RPC API, e.g. 8571, 8570.
 - Permitted transaction types, e.g. pay-to-address, pay-to-multisig, pay-to-script-hash.
 - Maximum block size, e.g. 1 megabyte.
 - Maximum metadata per transaction (OP_RETURN), e.g. 4096 bytes
 
 ## Setting up
 
 - Creating the Chain
     
  ```
   multichain-util create namchain
  ```

 - Running the daemon
 
 ```
   multichaind namchain -daemon

    MultiChain 2.1.2 Daemon (Community Edition, latest protocol 20012)

    Looking for genesis block...
    Genesis block found

    Other nodes can connect to this node using:
    multichaind namchain@169.254.31.2:7753

    This host has multiple IP addresses, so from some networks:
    multichaind namchain@192.168.43.172:7753

    Listening for API requests on port 7752 (local only - see rpcallowip setting)

    Node ready.
```
