# TP2 


## Question P2.1-i

The server that showed worst results was the server of the **Governament of Namibia**. <br>
This server does not support **Autenthicated Encryption (AEAD)**, which is the only encryption aproach without any known weaknesses. Without this aproach the server is vulnerable to **Timing Attacks**. It also does not use **Foward Secrecy**, a property of secure communication protocols. It protects passed sessions against future compromises of private-key. <br>
The server accepts **RC4-Cipher**, but only with older protocols. This cipher is demonstrably broken and unsafe to use in **TLS** as currently implemented, although the attack is not yet practical. <br>
It supports only older protocols, but not the best TLS1.2. Instead it uses TLS1.0, which is insecure and remains vulnerable to attacks, like the **Lucky 13 attack** .  <br>
Mozilla and Google distrust this server's certificate because it was issued by **Symantec** and they lost confidence in their cerficate issuance policies and practices. <br>
This server uses **SSL3**, that makes it vulnerable to the **POODLE Attack**. This attack will be explained in the next question. <br>
The last problem is that it supports insecure **Diffie-Hellman** key exchange parameters, making it vulnerable to the **Logjam attack** .  <br>
Because of all this problems, the final grade is **F**, making it especially insecure.  

## Question P2.1-ii

The **POODLE attack** is a problem in the CBC encryption scheme as implemented in the SSL3 protocol. To exploit this attack, the attacker must be able to inject malicious JavaScript in the victim's browser and also be able to observe and manipulate encrypted network traffic on the wire. <br>     
In pratical terms, this vulnerability allows a Man-in-the-middle attacker to decrypt ciphertext usins a padding oracle side channel attack. It is not easily accomplished because it requires a large amount of time and resources.    

## Question 3.1

We chose the Vodafone's and MEO's server located in Lisbon, with the following ip adresses 94.62.99.194 and 83.240.182.162, respectively. <br>

### 2
The Vodafone's server uses **OpenSSH 7.9** software. <br>
MEO's server uses **Dropbear SSH 2016.74** software.

### 3 - 4 - 5

The software with the most vulnerabilities is the **Dropbear SSH 2016.74**. It also has the most severe vulnerability with a score of 9.3. <br>
This vulnerability has a high score, making it dangerous because it impacts confidentiality, integrity and availability. The access complexity is medium and to exploit it is not needed any authentication and it gives admin access. <br>
Exploiting this vulnerability results in total iformation disclousure, revealing all system files. There is a total loss of system protection with the entire system being compromised. And finally, an attacker can take down the all system.  
  