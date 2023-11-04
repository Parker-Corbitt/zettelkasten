##  Midterm Study Guide Q/A

1) Which standards body that is part of the Department of Commerce issues Federal Information Processing Standards?

	- NIST
	- *Other notable orgs are ISOC (Internet Society, contains IETF), ISO (International Organization for Standards)

2) What Are the three elements of the CIA model?
	- Integrity
		- Data Integrity - Program changes are performed in an authorized, specified manner
		- System Integrity - Functions unimpaired, free from (un)intentional unathorized manipulation of the system
	- Availability
		- Systems work promptly and service is not denied
	- Confidentiality
		- Data Confidentiality - prevents disclosure of confidential information
		- Privacy - Individuals can control what information is collected and stored about them 

3) What is the ability to prove that you sent a message?

	  *Try to find where the difference is in implementation*
	- Authentication - Verifies the sender's identity and source of the message
	- NOTE - Non-repudiation is different in that it confirms the validity/integrity of the message

4) In order for a bug to be a vulnerability, it must have what two qualities?

	- Available
	- Exploitable

5) Give an example of a symmetric encryption algorithm discussed in class

	- DES - *block*
	- AES - *block*

6) Using a brute force attack, how many combinations of secret key would you have to try *on average* to break DES?

	- You are ***on average*** going to have to try around half the the available key space to break DES
$$ 2^{n-1}\ Where \ 'n'\ is \ the \ size \ of \ the \ key$$

7) What is the name of the Dutch algorithm used as the Advanced Encryption Standard?

	- Rijndael

8) Give 3 properties of a good hash function

	- Low collision rate
	- Impossible to derive input from output
	- Should be easy to compute for all values

9) Name the inventor(s) of public key cryptography

	- Diffie & Hellman

10) Give the truth table for XOR

| Input 1 | Input 2 | Output |  
| -------- | -------- | -------- |  
| 0 | 0 | 0 |  
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 | 

11) Summarize the steps of AES

	1) Key Mixing
	2) Substitution
	3) Permutation
	4) Repeat (*depending on key size*)

12) List one of the top 6 certificate authorities

	- IdenTrust
	- DigiCert

13) What is 23 mod inverse 5?

	- Pretty sure its 2 here

14) Give two examples of a way to perform a DOS attack

	- Ping Flooding
	- SYN Spoofing
	- Cyberslam
	- Poison Pill

15) How do you produce a digital signature for a message?

	- Hash it, then encrypt the hash with your private key


## Slide Notes

#### Security Requirements
- Access Control - Limit system access to authorized users/processes/and devices to their assigned level of access
- Certification, Accreditation, Security Assessments periodically evaluate level of protection
- Emergency Response = Contingency Planning
- Authenticate the proposed identities of everyone/thing trying to access information systems
- In general, make sure the people occupying positions of responsibility are well trained and trustworthy
- Risk Assessment - Assess the possible damage to assets, image, reputation resulting from the operation of information systems
- System & Information Integrity - Identify and correct flaws quickly, provide protection from malicious actors at proper points, take appropriate security responses
#### Attack Surfaces
- A vulnerability is both *available* and  *exploitable*
- Examples of such are 
	- services on open ports
	- interfaces to services
	- poorly written code
	- People
- 3 types of AS: SHN (Software, Human, Network)
- Attack Trees express the continued branching (nesting)  of  AS

#### Symmetric Encryption
- Uses a shared key and a reversible process
- Attacks: Cryptanalysis & Brute Force

#### Public Key Encryption
- Invented by Diffie and Hellman (and Merkle)
- Private first, great for auth
- Public second, great for configdentiality
- Should be
	- Inexpensive to gen
	- infeasible to derive any part if you have one part
- Rivest, SHamir, Adleman made RSA
- Digital signatures provide integrity and non-repudiation, but not confidentiality
##### DES
- Introduced by NISTin '77
- uses a 56 bit key, Triple can use 112 or 168 (AES uses 128, 192, 256)
- Rijndael replaces DES as the new standard

#### Stream Ciphers
- Change byte by byte
- can be done by using  rand

#### Auth & Hashing
- Auth - Being able to prove you are who you say you are
- Example hash alg is md5
- Means of Auth
	- Knows
	- Possesses
	- Is
	- Does
- Salting prevents rainbow table attacks

#### Diffie Hellman Handshake

***LOOK AT THIS***

