# Asymmetric Encryption

Why Asymmetric Encryption Exists

### Symmetric encryption has a problem:
- How do you share the secret key securely?

Asymmetric cryptography solves this.

## Public-Key Cryptography Concept

Each user has:
- Public key (shared)
- Private key (secret)

Data encrypted with one key can only be decrypted by the other.



## RSA
RSA (Rivest–Shamir–Adleman) is one of the oldest and most widely used public-key cryptography algorithms, relying on large prime factorization for secure data transmission. It uses a public key for encryption and a private key for decryption, making it fundamental to modern secure communications like HTTPS, digital signatures, and secure email.

RSA is based on the difficulty of factoring large numbers.

RSA security relies on:
- Difficulty of factoring large numbers

Public key:
- Easy to compute

Private key:
- Hard to derive

RSA is not used to encrypt large data due to performance.

RSA is mainly used for:
- Secure key exchange
- Digital signatures

### RSA Key Size
- 1024-bit → insecure
- 2048-bit → minimum standard
- 4096-bit → high security

Common RSA Mistakes
- Small key sizes
- Encrypting large files
- Reusing keys
- Poor random number generation
