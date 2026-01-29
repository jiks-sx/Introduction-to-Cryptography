# Digital Signature Lab

Sign file:
- openssl dgst -sha256 -sign private.key -out sign.bin secret.txt

Verify:
- openssl dgst -sha256 -verify public.key -signature sign.bin secret.txt
