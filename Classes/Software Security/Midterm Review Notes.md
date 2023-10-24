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