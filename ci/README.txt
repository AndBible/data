Encrypt:
openssl aes-256-cbc -a -salt -pbkdf2 -in testmods.zip -out testmods.zip.enc -pass "pass:$(cat passphrase.txt)"

Decrypt:
openssl aes-256-cbc -d -a -pbkdf2 -in testmods.zip.enc -out testmods-2.zip   -pass "pass:$(cat passphrase.txt)"


