[Information and Cyber Security Playlist] https://www.youtube.com/playlist?list=PLYwpaL_SFmcArHtWmbs_vXX6soTK3WEJw

http://www.crypto-it.net/eng/theory/index.html 

http://practicalcryptography.com/


---

CIA Triad The CIA triad in Cryptography 

https://www.geeksforgeeks.org/the-cia-triad-in-cryptography/

---

Before beginning, we define some terms. An original message is known as the
**plaintext**, while the coded message is called the **ciphertext**. The process of converting
from plaintext to ciphertext is known as enciphering or **encryption**; restoring the
plaintext from the ciphertext is deciphering or **decryption**. The many schemes used
for encryption constitute the area of study known as **cryptography**. Such a scheme
is known as a **cryptographic system** or a **cipher**. Techniques used for deciphering a
message without any knowledge of the enciphering details fall into the area of **cryptanalysis**.
Cryptanalysis is what the layperson calls “breaking the code.” The areas of
cryptography and cryptanalysis together are called **cryptology**.

**Cryptographic systems** are characterized along three independent dimensions:

1. **The type of operations used for transforming plaintext to ciphertext**. All
encryption algorithms are based on two general principles: **substitution**,
in which each element in the plaintext (bit, letter, group of bits or letters)
is mapped into another element, and **transposition**, in which elements
in the plaintext are rearranged. The fundamental requirement is that no
information be lost (i.e., that all operations are reversible). Most systems,
referred to as product systems, involve multiple stages of substitutions and
transpositions.
2. **The number of keys used**. If both sender and receiver use the same key, the
system is referred to as symmetric, single-key, secret-key, or conventional
encryption. If the sender and receiver use different keys, the system is referred
to as asymmetric, two-key, or public-key encryption.
3. **The way in which the plaintext is processed**. A block cipher processes the input
one block of elements at a time, producing an output block for each input
block. A stream cipher processes the input elements continuously, producing
output one element at a time, as it goes along.

---

- **Authentication**- It is any process by which a system verifies the identity of a user who wishes to access it.
- **Non- repudiation**– It means to ensure that a transferred message has been sent and received by the parties claiming to have sent and received the message. Non-repudiation is a way to guarantee that the sender of a message cannot later deny having sent the message and that the recipient cannot deny having received the message.
- **Integrity**– to ensure that the message was not altered during the transmission.

#### Symmetric Encryption 

A symmetric encryption scheme has five ingredients:

- ■ Plaintext: This is the original intelligible message or data that is fed into the
algorithm as input.
- ■ Encryption algorithm: The encryption algorithm performs various substitutions
and transformations on the plaintext.
- ■ Secret key: The secret key is also input to the encryption algorithm. The key is
a value independent of the plaintext and of the algorithm. The algorithm will
produce a different output depending on the specific key being used at the
time. The exact substitutions and transformations performed by the algorithm
depend on the key.
- ■ Ciphertext: This is the scrambled message produced as output. It depends on
the plaintext and the secret key. For a given message, two different keys will
produce two different ciphertexts. The ciphertext is an apparently random
stream of data and, as it stands, is unintelligible.
- ■ Decryption algorithm: This is essentially the encryption algorithm run in
reverse. It takes the ciphertext and the secret key and produces the original
plaintext.

[Symmetric (Private key Cryptographic) vs Asymmetric Encryption (Public Key Cryptographic)] https://www.ssl2buy.com/wiki/symmetric-vs-asymmetric-encryption-what-are-differences

[Difference between Private key and Public key Cryptography] https://www.geeksforgeeks.org/difference-between-private-key-and-public-key/

---

### Encryption Techniques - Substitution and Transposition

The two basic building blocks of all encryption techniques are substitution
and transposition

#### Substitution

A substitution technique is one in which the letters of plaintext are replaced
by other letters or by numbers or symbols. If the plaintext is viewed as a sequence
of bits, then substitution involves replacing plaintext bit patterns with ciphertext bit
patterns. **Caeser Cipher** is an example of substitution cipher. 


#### Transposition

A very different kind of mapping is achieved by performing
some sort of permutation on the plaintext letters. This technique is referred to as a
transposition cipher.
The simplest such cipher is the **rail fence technique**, in which the plaintext is
written down as a sequence of diagonals and then read off as a sequence of rows.

[Rail Fence Cipher – Encryption and Decryption] https://www.geeksforgeeks.org/rail-fence-cipher-encryption-decryption/

[Transposition Cipher | Keyless Transposition Technique Explained with Solved] https://www.youtube.com/watch?v=j7QdpHO5N8U

[Transposition Cipher | Columnar Transposition Technique Explained with Solved Example] https://www.youtube.com/watch?v=KczOjHHb5Nw

---

### Block vs Stream Cipher

Block Cipher Converts the plain text into cipher text by taking plain text’s block at a time. Eg, DES, AES, Blowfish    	   
Stream Cipher Converts the plain text into cipher text by taking 1 byte of plain text at a time.  Eg, FISH, RC4    

https://www.geeksforgeeks.org/difference-between-block-cipher-and-stream-cipher

[Block Cipher] https://youtu.be/aGxdQxO0nEo

A block cipher consists of two paired algorithms, one for encryption, E, and the other for decryption, D.[1] Both algorithms accept two inputs: an input block of size n bits and a key of size k bits; and both yield an n-bit output block

[What are stream ciphers] https://ctf101.org/cryptography/what-are-stream-ciphers/

[Stream Cipher] (must watch) https://youtu.be/dOKXCCwlwCk

#### Modes of Block Cipher 

[Block cipher modes of operation] (must read) https://www.geeksforgeeks.org/block-cipher-modes-of-operation/

http://www.crypto-it.net/eng/theory/modes-of-block-ciphers.html

- ECB - Electronic Code Book https://youtu.be/It0KU1kyMUQ
- CBC - Cipher Block Chaining https://youtu.be/fueyWs92cvs
- CFB - Cipher Feedback Mode https://youtu.be/QqcctEPQKuU
- OFB - Output Feedback Mode https://youtu.be/pypos_NnLfM
- CTR - Counter Mode https://youtu.be/6X1GkaJpBj0
--- 

### Hashing and Salting

A **hash function** `H` accepts a variable-length block of data `M` as input and produces
a fixed-size hash value `h = H(M)`. A “good” hash function has the property that the
results of applying the function to a large set of inputs will produce outputs that are
evenly distributed and apparently random. 

The kind of hash function needed for security applications is referred to as a
**cryptographic hash function**. A cryptographic hash function is an algorithm for which
it is computationally infeasible (i.e to find an attack significantly more efficient than
brute force) to find either (a) a data object that maps to a pre-specified hash result
(the one-way property) or (b) two data objects that map to the same hash result (the
collision-free property). Because of these characteristics, hash functions are often used
to determine whether or not data has changed

Applications of cryptographic hash functions:

- Message Authentication
- Digital Signatures
- Securing Password 

#### Message Authentication

Message authentication is a mechanism or service used to verify the integrity of
a message. Message authentication assures that data received are exactly as sent
(i.e., there is no modification, insertion, deletion, or replay). 

When a hash function is used to provide message authentication,
the hash function value is often referred to as a **message digest**.
The essence of the use of a hash function for message integrity is as follows. The sender computes a hash value as a function of the bits in the message and transmits both the hash value and the message. The receiver performs the same hash calculation on the message bits and compares this value with the incoming hash value. If there is a mismatch, the receiver knows that the message (or possibly the hash
value) has been altered. The hash value must be transmitted in a secure fashion. That is, the hash value
must be protected so that if an adversary alters or replaces the message, it is not
feasible for adversary to also alter the hash value to fool the receiver. 

 Message authentication is achieved using a message
 **authentication code (MAC)**, also known as a **keyed hash function**
 A MAC function takes as input a secret key and
a data block and produces a hash value, referred to as the MAC, which is associated with the protected message. If the integrity of the message needs to be checked,
the MAC function can be applied to the message and the result compared with the
 associated MAC value. An attacker who alters the message will be unable to alter the
associated MAC value without knowledge of the secret key. Note that the verifying
party also knows who the sending party is because no one else knows the secret key.

#### Digital Signature 

The operation of the digital signature is similar
to that of the MAC. In the case of the digital signature, the hash value of a message is encrypted with a user’s private key. Anyone who knows the user’s public key can
verify the integrity of the message that is associated with the digital signature. In
this case, an attacker who wishes to alter the message would need to know the user’s
private key. Note that, the implications of digital signatures go
beyond just message authentication.

#### Securing Passwords

https://auth0.com/blog/hashing-passwords-one-way-road-to-security/

https://auth0.com/blog/adding-salt-to-hashing-a-better-way-to-store-passwords/

[https://www.thesslstore.com/blog/difference-encryption-hashing-salting/] https://www.thesslstore.com/blog/difference-encryption-hashing-salting/

[What is Hashing] (Must Watch) https://www.youtube.com/watch?v=2BldESGZKB8

#### How are MAC and Digital Signature different

MACs differ from digital signatures as MAC values are both generated and verified using the same secret key. This implies that the sender and receiver of a message must agree on the same key before initiating communications, as is the case with symmetric encryption. For the same reason, MACs do not provide the property of non-repudiation offered by signatures specifically in the case of a network-wide shared secret key: any user who can verify a MAC is also capable of generating MACs for other messages. In contrast, a digital signature is generated using the private key of a key pair, which is public-key cryptography. Since this private key is only accessible to its holder, a digital signature proves that a document was signed by none other than that holder. Thus, digital signatures do offer non-repudiation.

https://security.stackexchange.com/questions/32114/what-is-the-difference-between-a-mac-and-a-digital-signiture

https://crypto.stackexchange.com/questions/5646/what-are-the-differences-between-a-digital-signature-a-mac-and-a-hash

---

[Digital Signatures and Certificates] https://www.geeksforgeeks.org/digital-signatures-certificates/


### Digital Signature

[Digital Signature] https://www.youtube.com/watch?v=y6e70OKHg7c

[How Digital Signatures Work] (Must Watch) https://www.youtube.com/watch?v=JR4_RBb8A9Q

A digital signature is a mathematical technique which validates integrity of a message, software or digital documents. A digital signature 
doesn't guarantee the authenticity of the message, meaning it can't make sure whether the message is from real owner or intended sender or not. It doesn't verify the
true identity of the sender and his public key, but use of Digital certificate does that. 

The steps which are followed in creating a digital signature are:

1. Select a file to be digitally signed.
2. The hash value of the message or file content is calculated. This message or file content is encrypted by using a private key of a sender to form the digital signature.
3. Now, the original message or file content along with the digital signature is transmitted.
4. The receiver decrypts the digital signature by using a public key of a sender.
5. The receiver now has the message or file content and can compute it.
6. Comparing these computed message or file content with the original computed message. The comparison needs to be the same for ensuring integrity.

<img width="650" src="https://user-images.githubusercontent.com/52335111/99152869-96316180-26ca-11eb-8d21-3e4134dd1f3b.PNG">

### Digital Certificate

[What is Digital Certificate] (Must Read) https://help.utk.edu/kb/index.php?func=show&e=1960

[Working of Digital Certificates Explained ] (Must Watch) https://www.youtube.com/watch?v=5rT6fZUwhG8

[Why digital certificate?] (Must Watch) https://www.youtube.com/watch?v=UbMlPIgzTxc

Digital certificates are electronic credentials that bind the identity of the certificate owner to a pair of electronic encryption keys, (one public and one private), that can be used to encrypt and sign information digitally. The main purpose of the digital certificate is to ensure that the public key contained in the certificate belongs to the entity to which the certificate was issued, in other words, to verify that a person sending a message is who he or she claims to be, and to then provide the message receiver with the means to encode a reply back to the sender.

The Certificate Authority (CA) packages together in the one certificate the public keys, information about the encryption algorithms used, the owner or subject data, the digital signature of a Certificate Authority that has verified the subject data itself, and a date range during which the certificate can be considered valid. Digital Certificates can be used for a variety of electronic transactions including e-mail, electronic commerce, groupware and electronic funds transfers.

The most widely accepted format for Digital Certificates is defined by the CCITT **X.509** international standard

[X.509] https://www.youtube.com/watch?v=JAgaWJivKwg

#### PKI (Public Key Infrastructure)

Terminology Related to PKI

- *Asymmetric Keys* - Two related keys, a public key and a private key, that are used to perform complementary operations, such as
encryption and decryption or signature generation and signature verification.
- *Public Key Certificate* - A digital document issued and digitally signed by the private key of a Certification Authority that binds the
name of a subscriber to a public key. The certificate indicates that the subscriber identified in the certificate
has sole control and access to the corresponding private key.
- *Public Key (Asymmetric) Cryptographic Algorithm* - A cryptographic algorithm that uses two related keys, a public key and a private key. The two keys have the
property that deriving the private key from the public key is computationally infeasible.
- *Public Key Infrastructure (PKI)* - A set of policies, processes, server platforms, software and workstations used for the purpose of administering certificates and public-private key pairs, including the ability to issue, maintain, and revoke public key
 certificates.
 
How does PKI Work?

Public Key Infrastructure uses Public Key Cryptography as the basis for providing encryption which uses asymmetric key algorithms to perform its role in which both communicating parties establish a working relationship by verifying each other’s identities. A framework of encryption that protects communications between the server (your website) and the client by:

- Establishing the identity of endpoints on a network
- Encrypting the flow of data via the network’s communication channels

The exchange of public keys before the symmetric encryption channel is established is facilitated by X.509 certificates and CA, only those public keys that have been signed by a Certificate Authority and bound to a certificate are considered acceptable for use online.

In broad terms, we can classify the use of **public-key cryptosystems** into
three categories: 

- ■ Encryption/decryption: The sender encrypts a message with the recipient’s
public key, and the recipient decrypts the message with the recipient’s private
key.
- ■ Digital signature: The sender “signs” a message with its private key. Signing
is achieved by a cryptographic algorithm applied to the message or to a small
block of data that is a function of the message.

- ■ Key exchange: Two sides cooperate to exchange a session key, which is a secret
key for symmetric encryption generated for use for a particular transaction (or
session) and valid for a short period of time. Several different approaches are
possible, involving the private key(s) of one or both parties/

Some algorithms are suitable for all three applications, whereas others can be
used only for one or two of these applications. Eg, `RSA` and `Elliptic Curve` encryption algorithms are suitable for all three applications,
whereas `DSS` is suitable in only Digital Signature application.

An example of *key exchange* PKI cryptosystem. Consider the following exchange which enables a server and a web application, for instance, a browser, to communicate with each other:

- When a browser wishes to establish a secure communication channel with a web server, it requests the server to present its public key.
- The server possesses an asymmetric public key, whose copy it presents to the browser.
- The browser generates a ‘session key’, a symmetric key that is encrypted using the public key that the server provided. This session key is then passed to the server.
- The web server, uses its private key to decrypt the session key which was encrypted by its public key by the client. If it is able to do this an encrypted channel with client is opened.

