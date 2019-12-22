# Cryptology
Cryptology, or cryptography, is the study of techniques that secure communication. In order to assure secure communications, there are three components required: **confidentiality**, **integrity**, and **availability**: 
* **Confidentiality** means that keeping or being kept secret or private. In secure communication, it means that the information is only viewable to the authenticated persons.\
Confidentiality is usually provided by encrypting the message with a cipher.

* **Integrity** means the quality of being honest and unified as a whole. In secure communication, it means that the authenticity of the given component is always true. In another word, we are always talking to someone who we expected, and the received message is always what the sender meant.\
Unlike confidentiality, integrity is not provided by cipher. We need to use something called **cryptographic hash function** to help us achieve this requirement.

* **Availability** means the quality of being able to be used or obtained. In secure communication, it means that the system should be always usable, which often means it sends message at real time.\
Availability is usually provided by the architecture of the secure communication system, which we do not covered.

In this project (more like codes for fun lol), I want to show some modern cryptologies as well as some techniques which helps in achieving online secure communications nowadays. I recommend using Java for this project and cryptology related stuff because Java has the most up-to-date cryptology libraries.

**I hope you guys enjoy it!**

## List of Topics:
* Classical Ciphers:
   * Caesar
   * Affine
   * Vigenere
* Symmetric Ciphers:
   * DES / AES
* Asymmetric Ciphers:
   * RSA
   * Chinese Remainder Theorem
   * Miller-Rabin Primality Test
* Cryptological Hash Fucntions and Applications:
   * Signature
   * MAC/HMAC

## Classical Ciphers
### Caesar Cipher
Caesar cipher is a stream, mono-alphabetic cipher with substitution. The way Caesar Cipher works is by shifting the alphabet down with a fix amount. To decrypt a Caesar cipher, ones can simply shift up the same amount, which is equivalent to shifting down the complement amount in the domain.
* Key: The shifting amount, an integer
* Encryption: `(plain_text + shift) % domain_size = cipher_text`
* Decryption: `(cipher_text + domain_size - shift) % domain_size = plain_text`

![Caesar cipher diagram](images/Caesar.png)
### Affine Cipher
Affine cipher is a stream, mono-alphabetic cipher with substitution. The way Affine Cipher works is similar to Caesar cipher, the different is that the shift amount will be determined by a linear equation instead of a number.
* Key: Two integers **a** and **b**, as the coefficients for a linear equation
* Encryption: `(a * plain_text + b) % domain_size = cipher_text`
* Decryption: `(cipher_text - b) / a % domain_size = plain_text`

Updated: 2019-12-22
