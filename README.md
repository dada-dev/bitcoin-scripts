# bitcoin-scripts
**Using your favorite programming language solves the following**

### Exercise 1: Build and Validate a P2PKH Script

**Goal:** Understand basic Bitcoin Script by constructing and validating a Pay-to-Public-Key-Hash (P2PKH) transaction output.

**Steps:**

1. **Generate a private key and derive its public key and hash:**
   - Generate a private key.
   - Derive the public key from the private key.
   - Compute the public key hash (e.g., RIPEMD-160(SHA-256(pubkey))).

2. **Construct a P2PKH locking script:**
   - `OP_DUP OP_HASH160 <pubKeyHash> OP_EQUALVERIFY OP_CHECKSIG`

3. **Simulate an unlocking script with a dummy signature and public key.**

4. **Write a function to “execute” the script:**
   - Push unlocking script items onto a stack.
   - Apply locking script opcodes (duplicate, hash, compare, check signature).
   - Return `True` if valid, `False` otherwise.


### Exercise 2: Simulate a 2-of-3 Multisig Transaction

**Goal:** Explore multi-signature setups by creating and spending a multisig output.

**Steps:**

1. **Generate 3 keypairs (private/public keys).**

2. **Build a 2-of-3 multisig locking script:**
   - `OP_2 <pubKey1> <pubKey2> <pubKey3> OP_3 OP_CHECKMULTISIG`

3. **Simulate spending with 2 signatures from any 2 keys.**

4. **Write a function to validate the multisig script execution.**


