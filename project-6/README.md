# Blockchain Developer Nanodegree Term 2

# Architect a Blockchain Supply Chain Solution - Part B

Supply Chain Solution

## The UML diagrams of this solution 

#### Activity Diagram
![Activity Diagram](https://github.com/djade007/supply-chain/blob/master/images/uml/1-activity-diagram.png?raw=true)

#### Sequence Diagram
![Sequence Diagram](https://github.com/djade007/supply-chain/blob/master/images/uml/2-sequence-diagram.png?raw=true)

#### State Diagram
![State Diagram](https://github.com/djade007/supply-chain/blob/master/images/uml/3-state-diagram.png?raw=true)

#### Class Diagram
![Class Diagram](https://github.com/djade007/supply-chain/blob/master/images/uml/3-uml-class.png?raw=true)

## Inheritance structure: 
```
contract AccessControl
contract Base is AccessControl
contract Core is Base
```
#### AccessControl - Collection of Contracts: 
These contracts manage the various addresses and constraints for the operations that can be executed only by specific roles.

There are 4 actors in a coffee supply chain:

- Farmer: The Farmer can harvest coffee beans, process coffee beans, pack coffee palettes, add coffee palettes, ship coffee palettes, and track authenticity.
- Distributor: The Distributor can buy coffee palettes and track authenticity.
- Retailer: The Retailer can receive coffee palettes and track authenticity.
- Consumer: The Consumer can buy coffee palettes and track authenticity.

#### Base - SupplyChain.sol: 
This is the most fundamental code shared throughout the core functionality. Which includes the main data storage, constants data types and internal functions for managing these items.

#### Core - Ownable.sol: 
The contract that controls ownership and transfer of ownership.

### Steps

Clone this repository:

```
git clone https://github.com/djade007/supply-chain
```

### Launch Ganache locally
```
ganache-cli -m "spirit supply whale amount human item harsh scare congress discover talent hamster"
```

In a separate terminal window:
```
cd project-6
```
```
truffle compile
```

Migrate smart contracts to the locally running blockchain, ganache-cli:
```
truffle migrate
```

Test smart contracts:
```
truffle test
```
All 10 tests should pass.

### Migration to Rinkeby Network
```
truffle migrate --reset --network rinkeby
```

### Launch DApp
In a separate terminal window, launch the DApp:
```
npm run dev
```

Then run the DApp in a browser - http://localhost:3000/

### Prerequisites

Please make sure you've already installed ganache-cli, Truffle and enabled MetaMask extension in your browser.

## Project Environment

- Truffle Version: 5.1.49
- Solidity Version: 0.5.16
- Node Version: 10.22.1
- Web3.js Version: 1.2.1
- truffle-hdwallet-provider Version: ^1.0.17"


## Project Results

### Deployed Contract Address:
(0x9F1ff4d6ee773EB9F36902B9C294b5b1f6925B9d)[https://rinkeby.etherscan.io/address/0x9F1ff4d6ee773EB9F36902B9C294b5b1f6925B9d]

### Transaction History
- Harvested - 0x22b1607edb78a2e47cc4f07c0af6978af617c6f14af7deaa9c87eb34c6c9ef8b
- Processed - 0xd1880df4b335a612b408a862a307e221eaba884ff729091a0a70acb4ea28b431
- Packed - 0x6a706e34e8c42f6fbd01857a405feafca2fece85e18ffc08d93166e67059d9d2
- ForSale - 0x60bfccec04956a1a2af289f1af162a93e0ed3bbbd144d24122b240ef5bad399d
- Sold - 0xb75658bba0855793821c49d0cd190e72555e6565fe968051ec9889d18f6ea781
- Shipped - 0x6cdf1862d3de3138d04da6b42188c1cec6f9fc46efc174eaa24964ee464ef5b6
- Received - 0xe813c09852eeb4c1019bbbf98cc4794962ec783fee6d38b58c64856f3d813ada
- Purchased - 0xeb47814b3982a8c940745c862a76c7cf08eb173e1312008d31d0cd8515c73d42
