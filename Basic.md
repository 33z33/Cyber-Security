
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



---

### Hashing and Salting

https://auth0.com/blog/hashing-passwords-one-way-road-to-security/

https://auth0.com/blog/adding-salt-to-hashing-a-better-way-to-store-passwords/

[https://www.thesslstore.com/blog/difference-encryption-hashing-salting/] https://www.thesslstore.com/blog/difference-encryption-hashing-salting/

[What is Hashing] (Must Watch) https://www.youtube.com/watch?v=2BldESGZKB8

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

<img src="https://media.geeksforgeeks.org/wp-content/uploads/3-56.png">

### Digital Certificate

[What is Digital Certificate] (Must Read) https://help.utk.edu/kb/index.php?func=show&e=1960

[Working of Digital Certificates Explained ] (Must Watch) https://www.youtube.com/watch?v=5rT6fZUwhG8

[Why digital certificate?] (Must Watch) https://www.youtube.com/watch?v=UbMlPIgzTxc

Digital certificates are electronic credentials that bind the identity of the certificate owner to a pair of electronic encryption keys, (one public and one private), that can be used to encrypt and sign information digitally. The main purpose of the digital certificate is to ensure that the public key contained in the certificate belongs to the entity to which the certificate was issued, in other words, to verify that a person sending a message is who he or she claims to be, and to then provide the message receiver with the means to encode a reply back to the sender.

The Certificate Authority (CA) packages together in the one certificate the public keys, information about the encryption algorithms used, the owner or subject data, the digital signature of a Certificate Authority that has verified the subject data itself, and a date range during which the certificate can be considered valid. Digital Certificates can be used for a variety of electronic transactions including e-mail, electronic commerce, groupware and electronic funds transfers.


The most widely accepted format for Digital Certificates is defined by the CCITT **X.509** international standard

[X.509] https://www.youtube.com/watch?v=JAgaWJivKwg


