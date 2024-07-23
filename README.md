# Salus Penetration Test
![Image text](/pic/back.png)
WEB3 penetration testing refers to the security testing of applications built using blockchain technology. The main goal is to find security vulnerabilities and provide repair suggestions.Our Web3 Penetration Testing not only uncovers vulnerabilities in your network, applications and cloud services but also focuses on middleware security and anti-tampering issues in the combined parts of Web2 and blockchain in your application.

## How is it different from smart contract auditing?
WEB3 penetration testing and smart contracts are two different technological domains. Although both are related to blockchain, they have different focuses and objectives. WEB3 penetration testing refers to the security testing of applications built using blockchain technology. These applications are typically based on Web3 technology and include centralized exchanges, cryptocurrency wallets, DEFI, GameFi, and other application types. The main goal of WEB3 penetration testing is to identify security vulnerabilities in the application and provide recommendations for fixing them.

## Contents：

[GameFi Risk](## Risks in GameFi) | [DeFi Risk] | [Cefi Risk] | [Social Media Risk] | [Research Article] | <a href="#A">Penetration testing report</a>

## <a name="D">Risks in GameFi</a>
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

### For example：
After finding the accurate address, it is possible to enable a speed boost feature to accelerate the game.
![Image text](/pic/game2.png)

The image below shows the effect of accelerating the game:

![Image text](/pic/game3.gif)

### Memory modification
Memory modification is a classic method of cheating in games, where the values of the game are modified in the memory. It is not feasible to validate every data coming from the client on the server side. Social games, for example, are often designed to earn in-game experience points or currency. These types of games typically have the main logic running on the client-side as a single-player game, with the final game score being uploaded to the server. The server then distributes the corresponding amount of in-game currency based on the game score. It is possible to search and modify the desired value in the memory before uploading the score.

Program implementation generally involves several key functions:

1.Reading process data: ReadProcessMemory

2.Search algorithm: Implemented based on value type, scan type, and memory scanning method

3.Writing data: WriteProcessMemory

There are several suggestions for defending against memory modification:

1.Splitting important values in memory: This makes it more difficult for cheaters to  locate and modify the values.

2.The default can be modified, and the upper limit of income is controlled on the server side.

### For example：
Download the game Bloons TD 6 and open it.

![Image text](/pic/game4.png)

Use Cheat Engine to select the game process to start modifying

![Image text](/pic/game5.png)

The value of the gold coins in the upper right corner of the current game is 2205.

![Image text](/pic/game6.png)

Use Cheat Engine to search for the value 2205.

![Image text](/pic/game7.png)

After the input is complete, click "First Scan".

![Image text](/pic/game8.png)

Change the value of the gold coin in some way. Here, a 100 gold coin equipment is purchased (the current value can be changed by earning gold coins and other means). At this time, the value of the gold coin becomes 2105, and the input value is 2105.

![Image text](/pic/game9.png)

![Image text](/pic/game10.png)

Click to scan again to determine the two memory addresses where the gold coin value is located.

![Image text](/pic/game11.png)

Click the address to display the memory information at this time.

![Image text](/pic/game12.png)

Add the relevant numerical addresses that need to be modified to the list.

![Image text](/pic/game13.png)

After selecting all, double-click the value to modify.

![Image text](/pic/game14.png)

After the operation, return to the game panel, the value of the game gold coin becomes the modified 989522.

![Image text](/pic/game15.png)

At this time, if you get a lot of gold coins, you can buy game props and characters at will, and you can successfully cheat in the game by modifying the memory value.

![Image text](/pic/game16.png)

## <a name="D">Risks in DeFi</a>

## <a name="C">Risks in Cefi</a>

## <a name="B">Risks in social media</a>
## <a name="A">Penetration Testing Report</a>

-----> [Entrance](/report/)



