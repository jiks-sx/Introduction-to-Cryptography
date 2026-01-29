# Cryptography Interview Questions – Detailed Answers

This document contains in-depth answers to common cryptography interview
questions. The explanations cover definitions, internal working,
security relevance, real-world usage, and interview-oriented insights.

---

## Q1: What is Encryption?

### Answer:

Encryption is the process of converting readable data, known as **plaintext**,
into an unreadable format called **ciphertext**, using a mathematical
algorithm and a secret value called a **key**.

The primary goal of encryption is to ensure **confidentiality**, meaning
that only authorized parties can access the original data.


### How Encryption Works (Conceptual Flow):

1. Plaintext data is taken as input.
2. An encryption algorithm applies mathematical transformations.
3. A cryptographic key controls the transformation.
4. The output is ciphertext, which appears random and unreadable.
5. Only someone with the correct key can decrypt the ciphertext back
   into plaintext.

### Why Encryption Is Important:

Encryption protects data:
- During transmission (data in transit)
- During storage (data at rest)

Without encryption:
- Attackers can read intercepted network traffic
- Stolen databases can expose sensitive information
- Privacy and trust on the internet collapse

### Real-World Examples:
- HTTPS encrypts web traffic
- Disk encryption protects laptops
- Messaging apps encrypt conversations
- VPNs encrypt network communication

### Interview Insight:
Encryption does **not** prevent data deletion or modification.
It specifically protects **confidentiality**.

---

## Q2: Symmetric vs Asymmetric Encryption

### Symmetric Encryption

#### Definition:
Symmetric encryption uses **a single shared secret key** for both
encryption and decryption.

#### How It Works:
- Sender encrypts data using the secret key
- Receiver decrypts data using the same key

#### Characteristics:
- Very fast and efficient
- Suitable for large amounts of data
- Requires secure key sharing

#### Common Algorithms:
- AES (Advanced Encryption Standard)
- DES (deprecated)
- 3DES (deprecated)

#### Use Cases:
- File encryption
- Disk encryption
- VPN data tunnels
- Database encryption

### Asymmetric Encryption

#### Definition:
Asymmetric encryption uses **two mathematically related keys**:
- Public key (shared openly)
- Private key (kept secret)

#### How It Works:
- Data encrypted with the public key can only be decrypted
  with the corresponding private key
- Data signed with the private key can be verified
  using the public key

#### Characteristics:
- Slower than symmetric encryption
- Solves the key distribution problem
- Enables authentication and digital signatures

#### Common Algorithms:
- RSA
- ECC (Elliptic Curve Cryptography)

#### Use Cases:
- Secure key exchange
- Digital signatures
- HTTPS certificate authentication

### Key Differences:

| Feature | Symmetric | Asymmetric |
|------|----------|------------|
| Keys | One shared key | Public & Private |
| Speed | Fast | Slow |
| Scalability | Difficult | Easy |
| Use | Data encryption | Key exchange & identity |

### Interview Insight:
Real-world systems use **hybrid encryption**, combining both types.

---

## Q3: What is Hashing?

### Answer:

Hashing is the process of converting input data of any size into a
**fixed-length value**, called a **hash**, using a mathematical
hash function.

Hashing is a **one-way process**, meaning the original data
cannot be reconstructed from the hash.

### Purpose of Hashing:

Hashing is used to ensure **data integrity**, not confidentiality.

It answers the question:
> “Has this data been modified?”

### Key Properties of Secure Hash Functions:

1. **One-way (Pre-image Resistance)**  
   It is computationally infeasible to reverse a hash.

2. **Collision Resistance**  
   Two different inputs should not produce the same hash.

3. **Avalanche Effect**  
   A small change in input results in a completely different hash.

### Common Hash Algorithms:

- MD5 – Broken (collision attacks)
- SHA-1 – Broken
- SHA-256 – Secure and widely used
- SHA-512 – Secure

### Real-World Uses of Hashing:

- File integrity verification
- Password storage
- Malware detection
- Digital signatures
- Blockchain

### Password Hashing (Important):

Passwords are **hashed, not encrypted**, because:
- Encryption is reversible
- Hashing is irreversible

Secure password storage uses:
- Hashing
- Salting
- Slow algorithms (bcrypt, Argon2)

### Interview Insight:
Hashing ensures integrity, **not confidentiality**.

---

## Q4: What is a Digital Signature?

### Answer:

A digital signature is a cryptographic mechanism that provides:
- **Authentication** (who sent the data)
- **Integrity** (data was not modified)
- **Non-repudiation** (sender cannot deny sending it)

### How Digital Signatures Work (Step-by-Step):

1. The sender hashes the original message.
2. The hash is encrypted using the sender’s **private key**.
3. The encrypted hash becomes the digital signature.
4. The message and signature are sent to the receiver.
5. The receiver decrypts the signature using the sender’s **public key**.
6. The receiver hashes the received message.
7. If both hashes match, the message is trusted.

### What Digital Signatures Prove:

- The sender owns the private key
- The message was not altered
- The sender cannot deny the action

### Real-World Uses:
- Software and code signing
- HTTPS certificates
- Secure email (PGP)
- Legal and financial documents

### Difference Between Encryption and Digital Signature:

| Encryption | Digital Signature |
|----------|------------------|
| Ensures confidentiality | Ensures authenticity & integrity |
| Uses recipient’s public key | Uses sender’s private key |
| Data is hidden | Data is verified |

### Interview Insight:
Digital signatures do **not encrypt data**.
They verify trust and authenticity.

## Final Interview Tip

If unsure during an interview, explain:
- The **security goal**
- The **problem being solved**
- The **real-world usage**

This demonstrates conceptual clarity, not memorization.
