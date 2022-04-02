# Review 1
## Off-the-Record Communication, or, Why Not To Use PGP
By Nikita Borisov, Ian Goldberg, Eric Brewer

### What is the problem?
The mechanisms currently used for social communications (such as PGP(Pretty Good Privacy) and S/MIME(public key encryption and signing of MIME data)) provide encryption (where keys are long-lived) and digital signatures (for the attainment of non-repudiability).

### Summary / Contribution
Online social communications should have perfect forward secrecy and repudiability (Off-the-Record conversation):

- To reduce the vulnerability of a compromised key; correspondents should re-key as frequently as possible disallowing the recovery of past or even future message transcripts encrypted using a longterm key (**Perfect forward secrecy**, attainment of confidentiality).
- Digital signatures prove the sender's authorship to anyone disregarding the correspondent's (sender's) cooperation in disclosal of this information (non-repudiability); thus, we authenticate using MAC keys banning the authorization of proofing the author to anyone (**repudiability**)

### Key Insights
- Diffie-Hellman key agreement protocol will be used to create the short-lived (generated when needed and discarded after use) encryption key in which redriving from any long-term key material is impossible.
- Malleable encryption is used (Malleable encryption scheme -  easy to alter the ciphertext to make meaningful changes in the plaintext) where stream ciphers (best suited for malleableness) and standardized AES counter mode is used (**forgeability** - for plausible deniability). 

### Notable design details/strengths 
- Most computing devices will be able to re-key with each message (even devices with limited computational power such as PDAs(personal digital assistants) should be able to do so within a minute)
- Only involved correspondents know of the shared secret MAC key and thus the recieving correspondent can assume the received message was from the correspondent he/she has shared the key with prior (attains inability to proof the author of a message leading to a point where the receiver could have made up the message themselves)

### Limitations/Weaknesses 
- It doesn't address the possibility of an adversary intercepting the messages and if the key for that partiular message on transit is then compromised the adversary can forge the Diffie-Hellman key and send it along (possibility of man-in-the-middle attack)

### Summary of Key Results (Up to 3 results)

### Open Questions (Where to go from here?)
