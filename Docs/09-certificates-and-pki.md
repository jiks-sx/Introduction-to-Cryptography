# Certificates and PKI
## Digital Certificates
Certificates bind a public key to an identity.

A certificate binds:
- Public key
- Identity
- Digital signature of trusted authority

### Certificate Authority (CA)

A trusted third party that:
- Verifies identity
- Signs certificates

Browsers trust pre-installed CAs.

### Certificate Chain
- Website → Intermediate CA → Root CA
- If chain breaks → HTTPS warning.


