# Nonrepudiation:
the process that verifies the message was sent by the sender and thus cannot be refuted

## Cryptology:
- cryptography + cryptanalysis
- science of encryption

## Cryptography:
- making and using codes to secure messages

## Cryptanalysis:
- cracking or breaking or decrypting encrypted messages

## Steganography:
- practice of representing information within another message or physical object, in such a manner that the presence of the information is not evident to human inspection.
- basically hiding a secret message in plain sight.
- hiding message in audio, video, image, text etc.

## Cryptovariable:
- key of your cryptography algorithm
- security of cyrptosystems depends on keeping key secret, not encryption algorithm secret.
- key length 64-bits is a good starting point

## Bit-stream cipher:
- cipher method where plaintext bit is transformed into cipher bit, one bit at a time.

## Block cipher:
- divide message into n-bit blocks
- transform each block into cipher bits using algorithm & key

## Cryptogram:

## Substitution cipher:
- substitute one value for another
### Monoalphabetic substitution:
- some letter is encrypted to the same letter each time
### Polyalphabetic substitution:
- some letter is encrypted to different letters each time
#### Example:
- Vigenère substitution: 26 x 26 table of letters shifted one place forward (actually, Google this to understand this)

## Transposition cipher:
- rearrange values within a block to create ciphertext
- can be done at bit or byte level
- use key & block sizes of 128+ bits for stronger encryption

## XOR cipher:
- XOR plain text bits
- simple to break
- do not use when transmitting sensitive data

## Vernam cipher:
- take an input of size n
- make a key of size n
- each of the letters in the alphabet are numbered
- bit-wise XOR the numbers of each i-th letter in input and key
- subtract 26 if the resulting number is >= 26, else leave it
- replace this number with the alphabet number it corresponds to

## Book-based cipher:
- Uses text in book as key to decrypt a message
### Book cipher:
- ciphertext is list of codes represting page, line and word numbers of the plaintext word from a book.
### Running key cipher: 
- similar to Vigenère cipher
- sequence of numbers from predetermined book tare used as the 'key' for breaking the cipher.
### Template Cipher:
- book/letter page with specific number of holes cut into it represent a message

## Cryptographic Algorithms
### Symmetric/Private-key:
- sender and receiver both must have same secret key
- fast
- if either key compromised, decryption easily possible
#### Examples:
- Data Encryption Standard (DES) - good
- Triple DES (3DES) - better
- Advanced Encryption Standard (AES) - best
### Assymetric/Public-key:
- one key to encrypt message (public)
- one key to decrypt message (private)
- used to create digital signatures
#### Examples:
- RSA
### Hybrid:
- assymetric + symmetric
#### Examples:
- Diffie-Hellman Key Exchange


## Public-Key Infrastructure (PKI):
-  Integrated system of software, encryption methodologies, protocols, legal agreements, and third-party services enabling users to communicate securely
- consists of certificate authority (CA) and registration authority (RA)

## Digital Certificates:
- e-document containing key and identifying information about entity that controls key
- digital signature of this file ensures integrity
- Distinguished name (DN) uniquely identifies a certificate entity
- different types of certificates based on different client-server apps

## Protocols for secure digital signatures:
### Digital Signature Standard (DSS)

## Protocols for secure internet connections:
### SSL (Secure Sockets Layer) protocol:
- use public-key encryption to secure channel over public internet
### HTTPS protocol:
- application of SSL over HTTP
### IPSec (Internet Protocol Security):
- open-source protocol framework
- uses Diffie-Hellman for internal network
- uses public-key encryption for key exchanges


## Protocols for secure wireless connections:
### WEP (Wired Equivalent Privacy):
- followed 8002.11 network protocol; it is broken now
- 40-bit key
- static key for everyone on network
- manual key distribution: type key into each device manually
### WPA and WPA2:
- basically better WEP
- 128-bit key
- dynamic keys: new key for user session and additional keys for each packet
- automatic key distribution
### WAP3:
- newest and better than WEP or WAP2
- uses SAE (Simultaneous Authentication of Equals) or Dragonfly
- stronger againts brute-force attacks and key-recovery attacks
### RSN (Robust Secure Networks):
- advanced wireless protocol
### CCMP (AES–Counter Mode CBC MAC Protocol):
- advanced wireless protocol

## Protocols for secure emails:
### PGP (Pretty Good Privacy):
- use IDEA cipher for message encoding
- open-source defacto standard for encryption and authentication of e-mail and file storage apps
###  S/MIME (Secure Multipurpose Internet Mail Extensions):
- encode using MIME + use digital signatures based on public-key cryptosystems
###  PEM (Privacy Enhanced Mail):
- use 3DES encryption + RSA for key exchanges & digital signatures
### IMAPS (Internet Message Access Protocol Secure):
- encrypted communication between email clients and servers
- prevents unauthorized monitoring or access to emails
### POP3S (Post Office Protocol Secure)
- same as IMAPs

## Protocols for secure web transactions:
### SET (Secure Electronic Transactions):
- use DES to encrypt credit card information transfers
- provides security for both internet-based payments and credit card swipe systems
- protect against e-payment fraud