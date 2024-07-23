# Risks in DeFi
DeFi projects should not only pay attention to the vulnerabilities related to smart contracts, but the security risks related to non-smart contracts are also fatal to DeFi applications.

### Front-end Malicious Script
Front-end Malicious Script: This malicious script will upload users' DASH coin account balance, keystore or private key, seed, and other critical information to a malicious address. A front-end vulnerability refers to a security flaw existing in the user interface or front-end code of a DeFi application, which may result in the theft or manipulation of users' funds or sensitive information by attackers. This includes malicious script injection, cross-site scripting (XSS), clickjacking, and more.

### For example:
There is an XSS vulnerability in the personal profile name field of a certain trading platform's backend. This vulnerability allows for the injection of malicious scripts.

![Image text](/pic/defi1.png)

Step 1 : Intercept the current data packet and insert malicious code after the name kite.

![Image text](/pic/defi2.png)

Step 2 :  Send data packets, view the status of the current web page, and successfully return the cookie information of the currently logged-in user.

![Image text](/pic/defi3.png)

Step 3 : Replace the payload with and wait for the XSS platform to receive it. When a user visits this page, the XSS platform can obtain the victim's user login credentials.

![Image text](/pic/defi4.png)

Step 4 : Copy the intercepted cookie and enter the command document.cookie information in the developer mode console to log in the user.

![Image text](/pic/defi5.png)

### Domain Hijacking
For example:

Step 1 : Access URL: https:/xx.com/

![Image text](/pic/defi6.webp)

Step 2 : Check the cname of xx.com in dashboard-xx.netlify.app.

![Image text](/pic/defi7.png)

Step 3 :  Create and deploy Nextjs application templates on https://www.netlify.com.

![Image text](/pic/defi8.png)

Step 4 : Add an additional subdomain under the Domain Management tab.

![Image text](/pic/defi9.png)

Step 5 : xx.com is added to the custom field. This extra subdomain will be set as the "main domain", and the netflix domain will be set as the "default subdomain".

![Image text](/pic/defi10.png)

Step 6 : Visit the URL https://xx.com, and its interface is changed to the Nextjs template set earlier.

![Image text](/pic/defi11.png)

At this time, the domain name has been successfully maliciously hijacked, which can require users to enter their mnemonic words or private keys, seeking to steal users' personal information and cryptocurrency wallet assets.

### Off-chain data source tampering

For example:

After the current user logs in, click My NFT, and you can see that the current user does not have any NFT assets.

![Image text](/pic/defi12.png)

Step 1 : Obtain other user addresses in the NFT market, and obtain the current user address from the link: 0xfB67dc...

![Image text](/pic/defi13.png)

Step 2 : Go back to my nft interface and click sale to capture the packet.

![Image text](/pic/defi14.png)

Step 3 : Replace useraddress with 0xfB67dc31....

![Image text](/pic/defi15.png)

Step 4 : Modify the message before sending the data.

Step 5 : Click Collection to obtain data information, and successfully switch to the NFT management background of user 0xfB67dc31..

![Image text](/pic/defi16.png)

By modifying the address of the data package, you can successfully exceed the authority to other accounts, and perform arbitrary casting or selling operations on other users' assets.

