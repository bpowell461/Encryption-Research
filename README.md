# Encryption Research Project

##   Abstract 
  The purpose of this project was to develop three encryption algorithms and test each one in different categories. Under the guidance of Dr. Andy Digh, the algorithms selected were: **RSA**, **SHA-256**, and **RC4**. The source code was written for each algorithm with only utilities classes imported for use. Each algorithm was then tested and rated in three categories: *Efficiency*, *Security*, and *Complexity*. 
  
  *Note: All source code is written in Java.*
  
##  Encryption Algorithms
Encryption Algorithms can be divided into three types: Asymmetric, Symmetric, and Hash Functions. 

 Asymmetric encryption, or public-key cryptography, uses a public and private key to encrypt and decrypt data. The keys used are numbers that are not identical to each other. As the name suggests, the public key is given to the public to encrypt data and the private is kept private to decrypt data.

 Symmetric encryption uses one private key to encrypt and decrypt data. The same key that is used to encrpyt data is also used to decrypt data. All keys in symmetric encryption are kept private.

 Hash Functions use no keys, instead they take a word or number and perform a hashing function in order to fix the data to an encrypted fixed size. The data in hash functions can not be decrypted, therefore hash functions are used to ensure that data has not been intercepted. 

### RSA
  The RSA algorithm, or Rivest–Shamir–Adleman  algorithm, was developed in 1977 and is one of the first asymmetric encryption algorithms used for cryptography. Although the algorithm is older, the RSA encryption algorithm still remains fairly secure. The RSA algorithm works as follows:
  * A user creates a public key based on two large prime numbers (n) and a common value of 65537 (e), the prime numbers are kept secret.
  * The public key is used to encrpyt a message 'm' with the equation `c = M^e (mod n)` where 'c' is the encrypted output.
  * The user uses the value of 'n' and the private exponent 'd' to create a private key.
  * The value of 'd' is generated by the equation `e^-1 (modulo λ(n))` where λ(n) is Carmichael's Totent.
  * The message 'c' is then decrpyted by the equation `c^d = m (mod n)`.
  
RSA is used mostly in 'https:' or sites that exchange personal information.
 
### RC4
  The RC4 algorithm, or Rivest Cipher 4 algorithm, is a symmetric encryption algoritm developed in 1994. The algorithm while slowly becoming outdated, remains fairly secure and is still widely used in systems. The RC4 is praised for being ridiculously fast and simple. The RC4 algorithm works as follows:
  * A random stream of bits is generated using a block of all 256 possible bytes (S) and two 8-bit pointers (i, j).
  * The random stream of bits is then combined with a user inputted key to produce a private key stream.
  * To encrypt data, the user takes a message 'm' and xors it with the bits of the keystream.
  * To decrypt the data, the user xors the bits of the encrypted message with the keystream. 
  
 RC4 is used mostly in WEP security for WiFi and in many banking systems.
  
### SHA-256
The SHA-2 algorithm, or the Secure Hash Algorithm 2, is a hash function developed by the NSA in 2001. The algorithm is the successor to SHA-1 and is used to verify data integrity. SHA-2 currently has six different methods SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, and SHA-512/256. The SHA-2 algorith works as follows:
  * Eight initial hashes are created by the first 32-bits of the first eight prime numbers
  * Sixty four round constants are created by the first 32-bits of the first sixty four primes
  * The input message is then padded to a length of a multiple of 512 bits with the last 64-bits the binary length of the message.
  * The word is then split into 32-bits each and bit-shifted and bit-rotated with the round constants.
  * The word is then added to the initial hashes and formed into a hash digest.
  
 The SHA-2 algorithm is most notably used in BitCoin as a 'proof-of-work'.
 
## Testing
The testing categories were divided into three seperate categories: *Efficiency*, *Security*, and *Complexity*.

### Efficiency
The efficiency of a program will refer to the speed of the program at a certain input size. Algorithms with a faster execution time performed on larger data will score higher in the efficiency category.

### Security
Security refers to the possibility that the algorithm can be broken. Algorithms that take longer to break or have a lower chance of being broken will score higher in the security category.

### Complexity
Complexity refers to the simpleness of the algorithm. Note that a program that has fewer lines of code does not mean that it is less complex. Simple algorithms will score higher in the complexity category.

## Results
Results for the Efficiency Test are found [here](EncryptionResearch/Project/Test Results.xlsx)
