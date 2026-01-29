# RSA Key Generation Lab

Generate private key:
- openssl genrsa -out private.key 2048

Generate public key:
- openssl rsa -in private.key -pubout -out public.key
