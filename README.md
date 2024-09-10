# Cryptography Basics: Key Exchange, Encryption, and Signing

This repository demonstrates basic cryptographic concepts using simplified implementations of Diffie-Hellman and RSA algorithms. It showcases key exchange, encryption, decryption, and digital signing processes, highlighting the roles of Alice, Bob, and Eve (an eavesdropper) in each scenario.

## Disclaimer

**IMPORTANT**: The implementations in this repository are greatly simplified and use small numbers for demonstration purposes only. They are NOT secure and should NEVER be used in real-world applications. This code is purely for educational purposes to illustrate basic cryptographic concepts.

## Scenarios

### 1. Diffie-Hellman Key Exchange

Demonstrates how two parties can establish a shared secret over an insecure channel.

**Principles:**
- Uses the difficulty of the discrete logarithm problem
- Allows key agreement without prior shared secret

**Steps:**
1. Alice and Bob agree on public parameters (prime p and base g)
2. Each generates a private key
3. Each computes and exchanges public keys
4. Each computes the shared secret

**Process:**
- Alice and Bob: Can compute the shared secret
- Eve: Can see all public information but cannot compute the shared secret

### 2. RSA Key Exchange

Shows how RSA can be used to exchange a symmetric key securely.

**Principles:**
- Uses the difficulty of factoring large numbers
- Allows secure key transmission using public-key cryptography

**Steps:**
1. Alice and Bob generate RSA key pairs
2. They exchange public keys
3. Bob generates a symmetric key
4. Bob encrypts the symmetric key with Alice's public key
5. Bob sends the encrypted key to Alice
6. Alice decrypts the key with her private key

**Process:**
- Alice: Can decrypt the symmetric key
- Bob: Can create and encrypt the symmetric key
- Eve: Can see the encrypted key but cannot decrypt it

### 3. RSA Encryption and Decryption

Demonstrates secure message transmission using RSA.

**Principles:**
- Asymmetric encryption
- Message confidentiality

**Steps:**
1. Bob prepares a message
2. Bob encrypts the message with Alice's public key
3. Bob sends the encrypted message to Alice
4. Alice decrypts the message with her private key

**Process:**
- Alice: Can decrypt the message
- Bob: Can encrypt the message
- Eve: Can see the encrypted message but cannot decrypt it

### 4. RSA Signing

Illustrates digital signature creation and verification.

**Principles:**
- Message integrity
- Non-repudiation
- Sender authentication

**Steps:**
1. Alice prepares a message
2. Alice signs the message with her private key
3. Alice sends the message and signature to Bob
4. Bob verifies the signature using Alice's public key

**Process:**
- Alice: Can sign messages
- Bob: Can verify Alice's signatures
- Eve: Can see signed messages and verify signatures, but cannot forge Alice's signature

## Results
![](https://github.com/ericyoc/key_exchanges_demo_poc/blob/main/key_exchanges_results_table.jpg)

Remember, never implement your own cryptography for real-world applications. Always use well-vetted, standard cryptographic libraries.
