# Symmetric Encryption

## Definition
Symmetric encryption uses one secret key for:
- Encryption
- Decryption

Security depends entirely on key secrecy, not algorithm secrecy.

This is called Kerckhoffs’s Principle.

AES (Advanced Encryption Standard)

AES is:
- A block cipher
- Works on fixed-size blocks (128-bit)
- Uses substitution and permutation rounds

AES key sizes:
- 128-bit
- 192-bit
- 256-bit

Why AES Is Trusted
- Publicly analyzed
- No practical attacks
- Used globally (banks, governments)

## Characteristics
- Fast and efficient
- Requires secure key sharing
- Used for large data encryption

## AES (Advanced Encryption Standard)
AES is a secure and widely used symmetric encryption algorithm.

Key sizes:
- 128-bit
- 192-bit
- 256-bit

AES Modes (Very Important)
- AES alone is NOT enough.
- Mode of operation matters.

| Mode | Secure | Reason                 |
| ---- | ------ | ---------------------- |
| ECB  | ❌      | Pattern leakage        |
| CBC  | ⚠️     | Needs IV               |
| GCM  | ✅      | Encryption + integrity |

Common Mistakes with Symmetric Crypto
- Reusing keys
- Weak passwords
- Using ECB mode
- Hardcoding keys

AES-GCM is the recommended mode for secure encryption.
