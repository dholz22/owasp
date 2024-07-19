## Crypthographic Failures (A2)

The use of weak, deprecated or incorrect cryptographic algorithms.

**Examples:**

- Sensitive data transmitted over a network without crypthography (HTTP, FTP, SMTP)
- Secret key or keys which can be predicted
- Use of older, weak, deprecated or incorrect encryption algorithms

**Bad Example:**

```
Cipher cipher = ...
Cipher.getInstance("DES/CBC/NoPadding");
Cipher.getInstance("DESede/CBC/PKCS5Padding");
Cipher.getInstance("AES/ECB/PKCS5Padding");
```

**Good Example:**

```
Cipher cipher = ...
Cipher.getInstance("AES/GCM/NoPadding")
```

### Why Are Crypto Failures Common?

- Crypto knowledge is rare
- The material to learn cryptography is very difficult
- It's hard to verify the level of security that crypto solutions provide
- It takes very senior and sophisticated developer resources

### Best Protection Strategies

- M: Manage keys and secrets properly
- U: Use up to date aand strong cryptographic algorithms, protocols and key sizes
- S: Sensitive data requires more protection, so classify them correctly
- I: Instrument encryption for data at rest and in transit
- C: Configure cryptographic protocols well

### AES: Advanced Encryption Standard Security

AES replaced DES in the early 2000s and today is considered the de-facto symmetric cipher to use, Selecting the correct mode of operation for AES is important in order for your implementation to be considered secure.

### What is Cipher?

In cryptography, a cipher is an algorithm for performing encryption or decryption—a series of well-defined steps that can be followed as a procedure. An alternative, less common term is encipherment. To encipher or encode is to convert information into cipher or code.
