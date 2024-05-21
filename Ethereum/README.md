# நம்Chain® Open Initiative Research Lab ![](https://img.shields.io/badge/Project-Nam-ff69b4.svg) ![](https://img.shields.io/badge/madeby-Ramaguru-blue.svg)

<p align="center">
<img src="https://1.bp.blogspot.com/-0SArWfduw68/XkxV8EmBBcI/AAAAAAAAABw/h9aWSWbm0J4kilgn3xddzQ3PdoP-e3RZgCLcBGAsYHQ/s1600/SAVE_20200127_132431.jpg" width="200" align="center">
</p>  

## Ethereum Blockchain Tutorials

A Repository dedicated to Ethereum Blockchain Tutorials.

## Prerequisite
- **Knowledge on**
    - HTML/CSS
    - JavaScript / Node.js
    - Blockchain Concepts
    
 - **Install**
    - Metamask Browser Extension (Firefox / Chrome / Brave Browsers)
    - [IPFS Companion Browser Extension](https://ipfs.io/)
    - [IPFS Desktop](https://ipfs.io/)
    - Web Service like XAMPP 
    
## Tutorial Topics
  - [Ethereum Blockchain Overview](#ethereum-blockchain-overview)
  - [Solidity Programming Language Basics](#solidity-programming-basics)
  - [Metamask and Faucet](#metamask-and-faucet)
  - [Infura Service](#infura-service)
  - [Web3.js Basics](Web3js-basics)
  - [Interplanetary File System (IPFS)](#ipfs)
  - [CryptoTokens (ERC-20, ERC-721, ERC-1155)](#cryptotokens)
  - [Identity Management Standards (ERC-725 and ERC-735)](#identity-management-standards)
  - [Oracles](#oracles)
  - [Ganache](#ganache)
  - [Truffle](#truffle)
  - [Solidity Source Code Testing](#solidity-source-code-testing)
  - [Solidity Vulnerability Analysis](#solidity-vulnerability-analysis)
  - [Examples](#examples)
      
## Ethereum Blockchain Overview

<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6f/Ethereum-icon-purple.svg/330px-Ethereum-icon-purple.svg.png" width="200" align="center">
</p>  

**Ethereum** is a second generation Blockchain Technology which is widely referred to as *World Computer*. The native cryptocurrency of the Ethereum Blockchain is called **"Ether (ETH)"**. Ethereum also provides the users the programming capability through its Smart Contract Programming. **Distributed Application (DApps)** can be developed using the smart contracts which is deployed and runs on the Ethereum Blockchain. 

Ethereum Blockchain uses **Ethereum Virtual Machine (EVM)** to execute the transactions. Ethereum uses memory-based Proof of Work (PoW) consensus algorithm. It also offers multiple testnets (Ropsten, Goerli, Kovan, Rinkeby) and private blockchain (Ganache) & Truffle Framework support for the development and testing of smart contracts. 

## Solidity Programming Basics

**Solidity** is the dedicated programming language for development of Smart Contracts on Ethereum Blockchain. Solidity is similar to Object Oriented Programming Language like Java / C++. ***Contract*** is the main component in the solidity programming which is similar to ***Class*** in Java. Like, Java, the solidity program on compilation is converted into bytecode for execution in EVM.  

For development of Smart Contracts using Solidity, Ethereum provides its own online IDE called [Remix](https://remix.ethereum.org/).

Below code shows the Solidity Template for your reference.

```
Filename: Sample.sol


// SPDX-License-Identifier: GPL-3.0

pragma solidity >=0.4.22 <0.7.0;
import "<<path-or-link-to-file-to-be-imported>>"

/**
 * @title Solidity Template
 * @author Ramaguru Radhakrishnan
 */
 contract <<contractName>> {
 
    mapping(datatype => datatype) public mapvar1; //Mapping to store a Key-Value 

    uint64 intvar1;	// Variable of Unsigned Integer with 64 bits 
    uint128 intvar2;    // Variable of Unsigned Integer with 128 bits
    int256 intvar3;     // Variable of Signed Integer with 256 bits
    
    string  stringvar;	// Variable of String
    
    address addressvar; // Variable of Address - to store Ethereum Wallet Address or Smart Contract Address
    
    address owner; // For assigning owner of the smart contract
    
    struct structvar {
        
        uint256 structvar1;
        string  structvar2;
    }
    
    structvar varstruct;
    
    /** Constructor */
    constructor() {}
    
    /** modifier to provide access control **/
    modifier isOwner() {
        // If the first argument of 'require' evaluates to 'false', execution terminates and all changes to the state and to Ether balances are reverted.
        require(msg.sender == owner, "Caller is not owner");
        _;
    }
    
    
    /**
     * @dev Example Function to perform operation and store (only owner can make a successful call)
     * @param num value to store
     */
    function <<functionName>>(paramaters) public isOwner {
        // do function operations
    }
    
     /**
     * @dev Example Function to return values
     * @param num value to store
     */
    function <<functionName1>>() public view returns(datatypes) {
        return (variables);
    }

}


```

On **Compilation** of Solidity Program, we get **ABI (Application Binary Interface)** along with Bytecodes. ABI is similar to API. On Running the Smart Contract, which actually **deploys** the Smart Contract on to the Blockchain, we get **Smart Contract Address**. These are the two important details required for accessing the Contract from the WebUI or FrontEnd in general.

## Testnet
A Testnet is a safe, secure and cost-effective testing (blockchain) network primarily used for dApps development, testing smart contracts, protocol upgrade, and staking. This is alternative to the mainnet where the tokens/currency are not real.

| Testnet Name | Consensus Mechanism | Date of Launch | Network ID | Purpose | Deprecated On | Notes |
|--------------|---------------------|----------------|------------|---------|---------------|-------|
| Olympic      | PoW (Proof of Work) | May 2015       | 0          | Initial testing phase for Ethereum before mainnet launch | July 2015 | Referred as Ethereum 0.9 |
| Morden       | PoW (Proof of Work) | August 2015    | 2          | First long-running public testnet after Olympic | November 2016 | | 
| Ropsten      | PoW (Proof of Work) | November 2016  | 3          | General purpose testnet, mimics Ethereum mainnet | December 2022 | Named after a Metro Station in Stockholm, Sweden |
| Kovan        | PoA (Parity)        | March 2017     | 42         | High stability and resilience for dapp testing | TBD (2024) | Named after a Station in Hougang, Singapore|
| Rinkeby      | PoA (Clique)        | April 2017  | 4          | Dapp development, stable testnet with reduced risk of spam | TBD (2024) | Named after a Metro Station in Stockholm, Sweden |
| Goerli       | PoA (Clique)        | March 2019     | 5          | Cross-client testing, unified testnet for multiple clients | Active |

| **Sepolia**      | PoS (Proof of Stake) | October 2021   | 11155111   | Testing Ethereum's transition to PoS, merge testing | Active |
| **Holesky**       | PoS (Proof of Stake) | September 2023   | 17000   | Testing Ethereum's transition to PoS, merge testing | Active |

## Metamask and Faucet

**Metamask** is a Browser Extension, is a tool which acts as a bridge for communication between the traditional browser to the blockchain (Distributed Web). Web3.js is used in the User Interface Component to enable communication with the Blockchain via Metamask. Metamask also has an inbuilt Wallet which on installation creates a Ethereum Wallet Address (identified by Hex numbers). More on Metamask is [here](https://namchain.blogspot.com/p/metamask.html).

<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/3/36/MetaMask_Fox.svg" width="200" align="center">
</p>  

**Faucet** is a developer support system which provides the Ether for development and testing purposes to our wallet address. [Click Here](https://faucet.metamask.io/) to access the Faucet and get your Test Ether. 

## Infura Service

**Infura** is a Ethereum and IPFS Service provider. Instead of running our own Ethereum and IPFS node at local machine, we can use their service through the APIs. You can [signup](https://infura.io/) to use their service.

## Web3.js Basics

**Web3.js** is a collection of javascript libraries which enables communication with local or remote Ethereum using HTTP or RPC communication. 

Below Web3.js code should be included in your HTML page to detect and define the Web3 Communication.

```
    <script src="https://cdn.jsdelivr.net/npm/web3@1.2.8/dist/web3.js"></script>
    <script>	
	
	var account;
	window.addEventListener('load', async () => {

	
		if (typeof window.ethereum !== 'undefined') { 
			console.log("MetaMask is Available :) !"); 
			}
			
		// Modern DApp browsers
		if (window.ethereum) {
			window.web3 = new Web3(ethereum);
			
			// To prevent the page reloading when the MetaMask network changes
			ethereum.autoRefreshOnNetworkChange = false;
			
			// To Capture the account details from MetaMask
			const accounts = await ethereum.enable();
			account = accounts[0];
				
			}
		// Legacy DApp browsers
		else if (window.web3) {
			//window.web3 = new Web3(web3.currentProvider);
			window.web3 = new Web3(new Web3.providers.HttpProvider("https://ropsten.infura.io/v3/cbd9dc11b30147e9a2cc974be655ef7c")); 
			}
		// Non-DApp browsers
		else {
			console.log('Non-Ethereum browser detected. Please install MetaMask');
			}
			
			});
    </script>			

```

## IPFS

**Interplanetary File System** is a protocol and a peer-to-peer file sharing and storage distributed network. IPFS is a content-addressed system, where a file is identified by its hash. IPFS complements the Blockchain for storage. 

<p align="center">
<img src="https://docs.ipfs.io/images/ipfs-logo.svg" width="100" align="center">
</p>  

## CryptoTokens 
- ERC-20 - Fungible Tokens
- [ERC-721](http://erc721.org/) - Non-Fungible Tokens (NFT)
    - [Cryptokitties](https://www.cryptokitties.co/)
- ERC-1155 - Multi-Token 

**ERC - Ethereum Request for Comments** is a standard within Ethereum Blockchain similar to RFC's for Internet Engineering Task Force (IETF).

## Identity Management Standards
Identity Managment is one of the major challenges faced across the globe and in various application domain. Ethereum proposed two standards for Identity Management (ERC-725) and Claim verification (ERC-735). 

- **ERC-725** supports Self-Soverign Identity could describe a human, a group or organisation, machine, real-world objects. These are simply a proxy smart contract controlled by multiple keys and smart contracts. The advantage is the user manages their own identity.
- **ERC-735** is a associated standard for ERC-725 which allows to add or remove claim about an ERC-725 identity.
- **ERC-1056** is a lightweight DID-compliant Identity standard which use Ethereum address as the DID.

## Oracles

**Oracles** are third-party services available for smart contracts to get external information like prices, weather details, stock market details, etc., for processing and decision making. **Provable** is one of the leading oracle service provider for different blockchains including Ethereum, EOS, R3 Corda, Hyperledger Fabric. There are different datasources available, from which we can request information from any as needed.
	
	- URL 
	- random
	- computation
	- IPFS
	- WolframAlpha
	
## Ganache

**Ganache** is a personal blockchain for rapid Ethereum DApp from develop, deploy and test in safe environment. Ganache can mine, acts as a wallet which has 10 accounts each with 100 ETH Balance, allows the user to explore the blocks and transactions happened so far.

<p align="center">
<img src="https://www.trufflesuite.com/img/ganache-logo-dark.svg" width="100" align="center">
</p>  

## Truffle

**Truffle Framework** is the popular development framework for Etherum Blockchain which handles the complete smart contract life cycle management.

<p align="center">
<img src="https://www.trufflesuite.com/img/truffle-header.svg" width="200" align="center">
</p>  

```
npm install -g truffle
truffle unbox
truffle init
truffle compile
truffle migrate (deploy)
truffle develop
truffle console
truffle debug
truffle test
truffle publish
```
The developer can interact with the contract and test using the built-in truffle console. To start the truffle console use the below command

```
truffle console
```

## Solidity Source Code Testing
Solidity Program or Source Code has to be tested for logic errors, ensure best coding practices, proper memory usage and to detect privacy and security issues.
Through a dedicated unit test either through solidity or js, we can test the solidity code before deploying it in the Mainnet. 

Below you can see the Javascript based testing through Truffle Framework. The file should be placed in the **test** folder and shall be executed by the command 

```
truffle test
```

```
FileName: SampleTest.js


const contractvar = artifacts.require(<<contract-name>>);

contract("Testing Contract", async accounts => {
	
  it("Testcase 1", async () => {
    const instance = await contractvar.deployed();
    await instance.function1(param1);
    var output = await instance.function2.call();
    assert.equal(output, <<expected-result>>);
  });
  
  it("Testcase 2", async () => {

  });
  
  ...
  ...
  
  it("Testcase n", async () => {

  });

});
```


## Solidity Vulnerability Analysis

Smart Contracts as known is the contract agreed between the parties transacting on Ethereum Blockchain. The Smart contract and the values maintained by the contract are stored in this immutable ledger, so it is very important to ensure that the smart contract does not have any vulnerability. 

- [Ethereum Contract Library](https://contract-library.com/)
- [Smart Check](https://tool.smartdec.net/)
- [MythX](https://mythx.io/)


## Examples

- **MetaMask Connection**
   - [DApp](Simple%20DApps/NamChain_Tutorials_Metamask_Connection.html)
   
- **Fixed DataType** 
    - [FixedDataTypes.sol](https://ipfs.io/ipfs/QmVNUwqQSVBzUPhctxMaN9KtGN2vwMSCeVmHrT7b59VvZD)
   
- **String Operations** 
    - [Strings.sol](https://ipfs.io/ipfs/QmbXGErA1yKc6iE86wnty17uPBaknGLDVRMEHq3uZerujg)
    
- **Address Operations**
    - [Address.sol](https://ipfs.io/ipfs/QmeAZyziifLrozsX5daKGGNeCdXStS9HbBVToruwDaXuwW)
    
 - **Mapping**
    - [Registry.sol](https://ipfs.io/ipfs/Qmd73HXiwnhCsGZ7uqoT1QaUeikSg6j4A6fUdb5KGAKyMT)
        - [Contract Link](https://ropsten.etherscan.io/address/0x13248d484eecb610cad3e9e03f8e7b8d477193b2)
    - [Registry_Project.sol](https://ipfs.io/ipfs/QmPyLAAi5VXx7CmBjJQPojkshMNkbeRw1YAtUMQwCuUTid)
        - [Contract Link](https://ropsten.etherscan.io/address/0xce2b4087cec369d9ec2dfdece9296b36134ff4bb)    
	
  - **Access Modifiers**
    - [Access.sol](https://ipfs.io/ipfs/QmbmBgx8et5a9N5Q9DrQvsvXbQmbSpBMcrYZS3Y4SQRErE)
        - [Contract Link](https://ropsten.etherscan.io/address/0xef24ce272e971b7771c7ed5f16001295d5570932)	

- **Storage and Retrieval**
    - [DApp](Simple%20DApps/NamChain_Tutorials_Storage_Smart_Contract.html)
    - Storage.sol - Refer remix.ethereum.org
        - [Contract Link](https://ropsten.etherscan.io/address/0xb3c65fc8a5b71eb48a8c35c52232d989ca6a8205)
	
- **Class Room**
    - [DApp](Simple%20DApps/NamChain_Tutorials_Class_Room.html)
    - [class.sol](https://ipfs.io/ipfs/QmWu72jUh9ZV2tT2tr5GhU7yinY1Q1c4NCSePGC6kqLrnA)
    	- [Contract Link](https://ropsten.etherscan.io/address/0xb72b5e4d4be833dffe7b51a1435c15fbbf193c0f)

- **Money Transfer**
    - [Sender.sol](https://ipfs.io/ipfs/Qmf3Wd2jvt15TVycq65h7JobHuqoyzQ9E4MZJLNtshzbZR)
        - [Contract Link](https://ropsten.etherscan.io/address/0xc7fb9a8410e0b228abaa4fccd63a8b22164f00bf)
    - [Receiver.sol](https://ipfs.io/ipfs/QmaXQ5WFn12q7cXCRQyVV3XuBpkhZuPWHB66BLcgX7LVtY)
        - [Contract Link](https://ropsten.etherscan.io/address/0xf5dc36a0eeec4909f3e09cfdc9b29e2343a1c73c)
  
 - **Events and Notification**
    - [DApp](Simple%20DApps/NamChain_Tutorials_Events.html)
    - [Events.sol](https://ipfs.io/ipfs/QmTFCP8uyL4UFqUQqH9PsQYJhpxtLsHoA6pP5ZQMyAkaCp)
        - [Contract Link](https://ropsten.etherscan.io/address/0x7d35606eacac8652f2a38c5a52128100e6545871)
    - [NotificationReceiver.sol](https://ipfs.io/ipfs/QmbiMjH9UZi8yYoDG5J5V8Vz7CKUD9d5K4rCUR8H92Z1Q4)
        - [Contract Link](https://ropsten.etherscan.io/address/0xe266c99a858aef94edb852709d79bf04771dc74f)
          
  - **ERC721 NFT - RAMCoin**     
    - [DApp](Simple%20DApps/NamChain_Tutorials_RAM_ERC721_Token.html) 
    - [MyERC721Token.sol](https://ipfs.io/ipfs/QmaCKsKDWMK8nmip51YCBgaUakU6zErwBnM6i8NdgPhdna)
        - [Contract Link](https://ropsten.etherscan.io/address/0xecff6e3fdf43146ae8e5a093a82b922777218807)
        - [NFT Token Tracker](https://ropsten.etherscan.io/address/0xecff6e3fdf43146ae8e5a093a82b922777218807)
	
  - **ERC1155**     


  - **Oracles** 	
  
  
  - **Identity Management** 
  

- <b>One Click DApp</b> <br/>
    One Click DApp is a 3rd party service which generates a UI which can be accessed using a public link. 
    - [Store and Retrieve](https://oneclickdapp.com/learn-unit/)
    
    Note: One Click DApp is available as a plugin in RemixIDE.

- <b>DApp Hero</b> <br/> 
    DApp Hero is a 3rd party service which generates HTML page / Website based on your Smart Contract, enabling the developer in quick DApp creation.
    - [Store and Retrieve](Simple%20DApps/DAppHero_Example.html)

