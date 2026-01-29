# AES Encryption Lab

Create file:
echo "Secret data" > secret.txt

Encrypt:
- openssl enc -aes-256-cbc -salt -in secret.txt -out secret.enc

Decrypt:
- openssl enc -aes-256-cbc -d -in secret.enc -out decrypted.txt
