![Image text](/pic/back.png)
# Risks in social media
Decentralized blockchain products are prone to phishing attacks. Security issues in common crypto communication software require users to be more cautious.

### Introduction:
As social media continues to thrive, security issues are increasingly prominent. Social media often involves the collection, storage, and sharing of users' personal information, and the leakage and misuse of this information can pose serious threats to users' privacy and security. To protect user interests and ensure product safety and reliability, penetration testing in social media has become particularly important.

Penetration testing in social media is a method to assess product safety. It discovers potential vulnerabilities and security risks by simulating real hacker attacks.

### Discord phishing：
In the Discord community, you may come across similar messages claiming that you have won a prize, but they are actually disguised phishing links.

![Image text](/pic/image1.png)

Clicking on the link takes you to a website that appears similar to Discord and prompts for authorization.

![Image text](/pic/image2.png)

After clicking on the authorization, another Discord login window pops up.

![Image text](/pic/image3.webp)

The window page appears very similar to the legitimate Discord login window, with minimal differences. The official login window image is as follows:

![Image text](/pic/image4.webp)

The current Discord login window appears as a new window within the browser, but we are unable to drag it outside the current browser window. Upon inspecting the page source code, it is discovered that it is an embedded interface rather than a new window. There are also some suspicious signs in the displayed address. The address "https:\discord.com\login" uses backslashes () for connections, while the official login address "https://discord.com/login" uses forward slashes (/) for navigation.

![Image text](/pic/image5.webp)

Once users enter their account username and password on this phishing page, their personal account will be immediately compromised, and the sensitive information will be exposed. Subsequently, fraudsters can use this information to gain unauthorized access to the user's account and engage in fraudulent activities.

### Twitter phishing：
Airdrops and free NFTs are areas of great interest for many people. Scammers take advantage of hijacked verified Twitter accounts to launch campaigns and redirect users to phishing websites.

![Image text](/pic/image6.avif)

Scammers exploit the assets of legitimate NFT projects to create phishing websites.

![Image text](/pic/image7.png)

They utilize popular services like Linktree to redirect users to fake pages that mimic NFT markets such as OpenSea and Magic Eden.

![Image text](/pic/image8.png)

Attackers will attempt to convince users to connect their cryptocurrency wallets (such as MetaMask or Phantom) to the phishing website. Unsuspecting users may unknowingly grant permission to these phishing websites to access their wallets. Through this process, scammers can transfer out cryptocurrencies like Ethereum ($ETH) or Solana ($SOL), as well as any NFTs held in those wallets.

### Webpage tampering/fake phishing：
Scammers send phishing emails and links with subject lines such as "Don't miss out on the limited-time OpenAI DEFI token airdrop." The phishing email claims that GPT-4 is now exclusively available to those who possess OpenAI tokens.

![Image text](/pic/image9.png)

After clicking on the "Get Started" button, you are redirected to the phishing website. It's important to note that the domain name uses hyphens, making the first part of the URL appear as if the main domain is "openai.com." This is achieved by using the subdomain "openai" and the second level ".com-token" followed by the top-level domain ".info."

![Image text](/pic/image10.png)

Connecting your wallet to the phishing website.

![Image text](/pic/image11.png)

Users are lured to click on the "Click Here to Claim" button, and upon clicking, they are given the option to connect using popular cryptocurrency wallets like MetaMask or WalletConnect.

![Image text](/pic/image12.png)

Once connected, the phishing website is capable of automatically transferring all cryptocurrency tokens or NFT assets from the user's wallet to the attacker's wallet, thereby stealing all the assets present in the wallet.

### Telegram phishing：
Scammers send private messages to users on Telegram with links to the latest "Avatar 2" movie, and the addresses appear to be simple and straightforward.

![Image text](/pic/image13.avif)

Upon opening the link, you arrive at a page with a seemingly genuine movie link, and you can even watch the video. However, at this point, the hacker has gained control over the user's browser.

![Image text](/pic/image14.png)

Entering the hacker's perspective, let's see how they use browser exploit tools to take control of your browser.

![Image text](/pic/image15.png)

Upon examining the hacker's control panel, it becomes apparent that they have access to all the information about the browsing user. This includes the user's IP address, cookies, proxy time zone, and more.

![Image text](/pic/image16.avif)

Upon inspecting the phishing link, it is discovered that the link points to a remotely loaded JavaScript script. The hacker controls the browser remotely by executing the script's content.

![Image text](/pic/image17.avif)

The hacker has the ability to switch to a Google Mail phishing interface and execute phishing attacks targeting Gmail users.

![Image text](/pic/image18.avif)

At this point, the front-end interface changes to a Google Mail login page. Users enter their account credentials and click on the login button.

![Image text](/pic/image19.avif)

In the background, the hacker successfully receives the login username and password.

![Image text](/pic/image20.avif)

Use this method to maliciously obtain user account and password information, resulting in the eventual exposure of user information and financial losses.
