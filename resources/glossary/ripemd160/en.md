---
term: RIPEMD160
---

Acronym for *Research and development in Advanced Communications technologies in Europe Integrity Primitives Evaluation Message Digest 160*. It is a cryptographic hash function that generates a 160-bit digest from an arbitrary input. It is used in Bitcoin to transform a public key into a receiving address for Legacy and SegWit v0 standards (for SegWit v1, the public key is not hashed). The process first involves applying the `SHA256` hash function to the public key, followed by the application of `RIPEMD160` on the result. This combination of two distinct hash functions is known as `HASH160` in the context of Bitcoin. `RIPEMD160` is also used in deterministic and hierarchical wallets to calculate key fingerprints. Specifically, `HASH160` is used to calculate the fingerprint of a parent key, then included in the metadata of an extended key (xpub, xprv...).
