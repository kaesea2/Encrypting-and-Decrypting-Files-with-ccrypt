# Encrypting and Decrypting Files with ccrypt

ccrypt is based on the Rijndael cipher, which provides strong security against brute force attacks and meets the Advances Encryption Standard (AES). its a symmetric key encryption (i.e same key for encryption and decrypting)

for this task, we’ll create a file and add content to it, then use ccrypt to encrypt, change its encryption key and decrypt it.

install ccrypt

```bash
apt-get install ccrypt
```

![Untitled](Encrypting%20and%20Decrypting%20Files%20with%20ccrypt%20eea4c6d52903406f9f4013f1a57b5383/Untitled.png)

to see the help menu

```bash
ccrypt -h
```

![Untitled](Encrypting%20and%20Decrypting%20Files%20with%20ccrypt%20eea4c6d52903406f9f4013f1a57b5383/Untitled%201.png)

next we’ll create a file to test the encryption

```bash
echo "this is super secret information" > testfile
cat testfile
ccrypt testfile
```

when prompted, enter a password. for this test purpose, i entered 123456789 as my password

```bash
ls
cat testfile.cpt
```

![Untitled](Encrypting%20and%20Decrypting%20Files%20with%20ccrypt%20eea4c6d52903406f9f4013f1a57b5383/Untitled%202.png)

to cat the file content using ccrypt and enter the password 123456789

```bash
ccat testfile.cpt
```

![Untitled](Encrypting%20and%20Decrypting%20Files%20with%20ccrypt%20eea4c6d52903406f9f4013f1a57b5383/Untitled%203.png)

changing the encryption key

```bash
ccrypt -x testfile.cpt
```

![Untitled](Encrypting%20and%20Decrypting%20Files%20with%20ccrypt%20eea4c6d52903406f9f4013f1a57b5383/Untitled%204.png)

use ccat to read the file again and confirm the key change

```bash
ccat testfile.cpt
```

![Untitled](Encrypting%20and%20Decrypting%20Files%20with%20ccrypt%20eea4c6d52903406f9f4013f1a57b5383/Untitled%205.png)

decrypting the file

```bash
ccrypt -d testfile.cpt
```

![Untitled](Encrypting%20and%20Decrypting%20Files%20with%20ccrypt%20eea4c6d52903406f9f4013f1a57b5383/Untitled%206.png)
