# NamChain - Open Initiative Research Lab ![](https://img.shields.io/badge/Project-Nam-ff69b4.svg) ![](https://img.shields.io/badge/madeby-Ramaguru-blue.svg)

<p align="center">
<img src="https://1.bp.blogspot.com/-0SArWfduw68/XkxV8EmBBcI/AAAAAAAAABw/h9aWSWbm0J4kilgn3xddzQ3PdoP-e3RZgCLcBGAsYHQ/s1600/SAVE_20200127_132431.jpg" width="200" align="center">
</p>  

## Ethereum Blockchain Tutorials

This repository is dedicated to Ethereum Blockchain. Here you can find examples related to Smart Contracts and DApps.

## Prerequisite
- Knowledge on 
    - HTML
    - CSS
    - JavaScript / Node.js
    
 - Install
    - Metamask Browser Extension (Firefox / Chrome / Brave Browsers)
    - [IPFS Companion Browser Extension](https://ipfs.io/)
    - [IPFS Desktop](https://ipfs.io/)
    - Web Service like XAMPP 
    
 ## Tutorial Topics
  - Ethereum Blockchain Overview
  - Solidity Programming Language Basics
  - Metamask and Faucet
  - Infura Service
  - Web3.js Basics
  - Interplanetary File System (IPFS)
  - CryptoTokens (ERC-20, ERC-721, ERC-1155)
  - Identity Management Standards (ERC-725 and ERC-735)
      
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
pragma solidity >=0.4.22 <0.7.0;

/**
 * @title Solidity Template
 * @author Ramaguru Radhakrishnan
 */
 contract <<contractName>> {

    uint64 intvar1;	// Variable of Unsigned Integer with 64 bits 
    uint128 intvar2;    // Variable of Unsigned Integer with 128 bits
    int256 intvar3;     // Variable of Signed Integer with 256 bits
    
    string  stringvar;	// Variable of String
    
    address addressvar; // Variable of Address - to store Ethereum Wallet Address or Smart Contract Address
    
    struct structvar {
        
        uint256 structvar1;
        string  structvar2;
    }
    
    structvar varstruct;
    
    /** Constructor */
    constructor() {}
    
    /**
     * @dev Example Function to perform operation and store
     * @param num value to store
     */
    function <<functionName>>(paramaters) public {
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

## Metamask and Faucet

**Metamask** is a Browser Extension, is a tool which acts as a bridge for communication between the traditional browser to the blockchain (Distributed Web). Web3.js is used in the User Interface Component to enable communication with the Blockchain via Metamask. Metamask also has an inbuilt Wallet which on installation creates a Ethereum Wallet Address (identified by Hex numbers). More on Metamask is [here](https://namchain.blogspot.com/p/metamask.html).

<p align="center">
<img src="https://metamask.io/images/mm-logo.svg" width="200" align="center">
</p>  

**Faucet** is a developer support system which provides the Ether for development and testing purposes to our wallet address. [Click Here](https://faucet.metamask.io/) to access the Faucet and get your Test Ether. 

## Infura Service

**Infura** is a Ethereum and IPFS Service provider. Instead of running our own Ethereum and IPFS node at local machine, we can use their service through the APIs. You can [signup](https://infura.io/) to use their service.

## Web3.js

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

## Tokens 
- ERC-20 - Fungible Tokens
- [ERC-721](http://erc721.org/) - Non-Fungible Tokens (NFT)
    - [Cryptokitties](https://www.cryptokitties.co/)
- ERC-1155 - Multi-Token 

**ERC - Ethereum Request for Comments** is a standard within Ethereum Blockchain similar to RFC's for Internet Engineering Task Force (IETF).

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

- <b>One Click DApp</b> <br/>
    One Click DApp is a 3rd party service which generates a UI which can be accessed using a public link.
    - [Store and Retrieve](https://oneclickdapp.com/learn-unit/)

- <b>DApp Hero</b> <br/> 
    DApp Hero is a 3rd party service which generates HTML page / Website based on your Smart Contract, enabling the developer in quick       DApp creation.
    - [Store and Retrieve](Simple%20DApps/DAppHero_Example.html)

# License

[MIT](https://github.com/ramagururadhakrishnan/NamChain/blob/master/MIT)
