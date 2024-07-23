# Salus-penetrationtest
![Image text](/pic/back.png)
WEB3 penetration testing refers to the security testing of applications built using blockchain technology. The main goal is to find security vulnerabilities and provide repair suggestions.Our Web3 Penetration Testing not only uncovers vulnerabilities in your network, applications and cloud services but also focuses on middleware security and anti-tampering issues in the combined parts of Web2 and blockchain in your application.

## How is it different from smart contract auditing?
WEB3 penetration testing and smart contracts are two different technological domains. Although both are related to blockchain, they have different focuses and objectives. WEB3 penetration testing refers to the security testing of applications built using blockchain technology. These applications are typically based on Web3 technology and include centralized exchanges, cryptocurrency wallets, DEFI, GameFi, and other application types. The main goal of WEB3 penetration testing is to identify security vulnerabilities in the application and provide recommendations for fixing them.

## View typical risks in different project types：

#### Risks in GameFi
#### Risks in DeFi
#### Risks in Cefi
#### Risks in social media

## Risks in GameFi
GameFi applications are considered high-risk areas for WEB3 penetration testing due to their large user base, diverse interaction scenarios, and the complexity of the games themselves.
### Introduction
In blockchain games, there are mainly two ways of communication: one way is through on-chain smart contracts to trigger changes in on-chain data, which are then listened to by off-chain applications to obtain data updates. The other way is to use Oracle services to introduce off-chain data into the blockchain, monitor data changes, and transmit them to smart contracts. During the communication process, there are security threats such as data tampering, communication interception, data forgery, Oracle attacks, and data privacy.

The majority of GameFi projects still rely on off-chain centralized servers for backend operations, network interfaces, and mobile applications. These centralized servers serve as centralized storage points for game data and user account information. They store critical information, and if these servers are compromised, attackers can gain access to this data and exploit vulnerabilities, resulting in information leaks and fund theft.
### The risk of data leakage in NFTs
The metadata of NFTs contains crucial descriptive information and is typically stored off-chain in the form of JSON files. However, many GameFi projects choose to store NFT metadata on their centralized servers instead of utilizing decentralized infrastructure. This approach increases the risk of tampering with the metadata by relevant parties or attackers.

The vulnerability CVE-2022-38217 exposes NFT-related information.
![Image text](/pic/game1.avif)
### Accelerated Cheating
Accelerated cheating is also commonly seen in multiplayer games. There are two cases of manipulating the speed of gameplay. One is using speed-up cheats, such as a speed gear, to accelerate the playback speed of Flash animations. The other case involves modifying the value of a variable in the game that controls the speed.

To detect cheats that accelerate Flash animations, we can compare the synchronization of the client and server time. When an abnormality is detected, we can prompt for image verification and interrupt the acceleration.

For cheats that manipulate speed through in-game variables, we should ensure protocol security to prevent modification of the corresponding values in the packet. Additionally, implementing SWF anti-reverse engineering protection can prevent modifications to the source code that controls the speed logic.

#### For example：
After finding the accurate address, it is possible to enable a speed boost feature to accelerate the game.
![Image text](/pic/game2.png)

![Image text](/pic/game3.gif)

![Image text](/pic/game4.png)

![Image text](/pic/game5.png)

![Image text](/pic/game6.png)

![Image text](/pic/game7.png)

![Image text](/pic/game8.png)

![Image text](/pic/game9.png)

![Image text](/pic/game10.png)

![Image text](/pic/game11.png)

![Image text](/pic/game12.png)

![Image text](/pic/game13.png)

![Image text](/pic/game14.png)

![Image text](/pic/game15.png)

![Image text](/pic/game16.png)

## Risks in DeFi

## Risks in Cefi

## Risks in social media

## Penetration testing report

-----> [Entrance](/report/)



