# Digital Signatures

## Purpose
Digital signatures provide:
- Authentication
- Integrity
- Non-repudiation

What a Digital Signature Proves

A digital signature proves:
- Who sent the data
- Data was not altered
- Sender cannot deny it

Signature Process 
- Hash message
- Encrypt hash using private key
- Send message + signature
- Receiver decrypts hash using public key
- Re-hash message
- Compare hashes

Match = trusted

### Why Digital Signatures Are Critical
- Software updates
- Code signing
- Financial transactions
- Legal documents


