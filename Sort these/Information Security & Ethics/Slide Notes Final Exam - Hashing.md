## Hash Function:
-  mathematical function
- takes input
- returns FIXED-SIZE string called 'hash' or 'digest'

### Uses:
In cryptography:
- message authentication
- digital signatures (for data integrity)
In databases:
- indexing
- searching

### Properties of Good Hash:
- deterministic: same input produces same output
- computationally efficient: reasonable time to compute
- difficult to reverse
- collision resistant: minimal likelihood of producing the same hash value for different inputs
- irreversible/one-wayness/pre-image resistance

## Irreversiblity of Hash:
- what makes it useful for storing passwords securely.
- hash stored in database instead of actual password.
### Benefits:
- Even after gaining access to password database, attacker cannot obtain original passwords easily.

## Cryptographic Hash Functions:
- MUST be irreversible/pre-image resistant
- designed to be secure
- ensure data integrity & authenticty
### Benefits:
- resist pre-image attacks
- resist collision attacks
- efficient for storing and comparing large amount of data due to fixed length output
### Weaknesses:
- computationally expensive
- SHA-1 is vulnerable to collision attacks and no longer secure
### Uses:
- digital signatures
- message authentication codes
- password storage
### Example:
- SHA-256
- SHA-3
- BLAKE2

## Non-cryptographic Hash Functions:
- may/may not be irreversible
- not necessarily designed to be secure
- used where security is NOT the primary concern
### Benefits:
- fast, computationally efficinet
### Weaknesses:
- not designed to be secure so are vulnerable to attacks
- not collision reistant
### Uses:
-  indexing and searching
### Example:
- Checksums
- CRC-32
- FNV hash

## Hash-based message authentication codes (HMACs):
- cryptographic hash functions
- verify integrity of messages
- use secret key to generate hash to check authenticity of message
### Benefits:
- resistant to pre-image attacks
- resistant to collision attacks
### Weaknesses:
- slower than non-keyed functions due to additional key input
- if secret key compromised then vulnerable

## Keyed Hash Functions:
- take input + secret key
- adds extra security
### Weaknesses:
- if secret key compromised, then vulnerable
- may be slower than non-keyed hash due to additional secret key input
### Uses:
- message authentication 
- integrity verification
### Examples:
- HMAC 
- Poly1305

## Perfect Hash Functions:
- guaranteed no collisions; unique hash for each input
### Benefits:
- absolutely collision-resistant
- efficinet for indexing/searching large data
### Weaknesses:
- difficult to construct, especially for large data
- less efficient than non-perfect hashes for SMALL data
### Uses:
- Generating hashtables for in computer programs

## Bloom Filters:
- probabilistic hash functions
- used to test whether an element is a member of a set
### Benefits:
- low probability of false negatives
### Weaknesses:
- may be false postiives, causing incorrect data retrieval or manipulation
- large storage required to maintain hash table
### Uses:
- databases + search engines to speed up queries