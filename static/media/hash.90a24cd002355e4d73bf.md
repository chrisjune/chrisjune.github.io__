Hash Generator
====================

MD5
---

The **MD5 message-digest algorithm** is a cryptographically broken but still widely used [hash function](/wiki/Hash_function "Hash function") producing a 128-[bit](/wiki/Bit "Bit") hash value. 

Although MD5 was initially designed to be used as a [cryptographic hash function](/wiki/Cryptographic_hash_function "Cryptographic hash function"), it has been found to suffer from extensive vulnerabilities. It can still be used as a [checksum](/wiki/Checksum "Checksum") to verify [data integrity](/wiki/Data_integrity "Data integrity"), but only against unintentional corruption. It remains suitable for other non-cryptographic purposes, for example for determining the partition for a particular key in a [partitioned database](/wiki/Partition_(database) "Partition (database)"), and may be preferred due to lower computational requirements than more recent [Secure Hash Algorithms](/wiki/Secure_Hash_Algorithms "Secure Hash Algorithms") algorithms.


MD5 was designed by [Ronald Rivest](/wiki/Ronald_Rivest "Ronald Rivest") in 1991 to replace an earlier hash function [MD4](/wiki/MD) and was specified in 1992 as RFC 1321.

One basic requirement of any cryptographic hash function is that it should be [computationally infeasible](/wiki/Computational_complexity_theory#Intractability "Computational complexity theory") to find two distinct messages that hash to the same value. MD5 fails this requirement catastrophically; such [collisions](/wiki/Collision_resistance "Collision resistance") can be found in seconds on an ordinary home computer.

On 31 December 2008, the [CMU Software Engineering Institute](/wiki/CMU_Software_Engineering_Institute "CMU Software Engineering Institute") concluded that MD5 was essentially "cryptographically broken and unsuitable for further use".
The weaknesses of MD5 have been exploited in the field, most infamously by the [Flame malware](/wiki/Flame_malware "Flame malware") in 2012. As of 2019, MD5 continues to be widely used, despite its well-documented weaknesses and deprecation by security experts.

SHA-1
---

In [cryptography](/wiki/Cryptography "Cryptography"), **SHA-1** (**Secure Hash Algorithm 1**) is a cryptographically broke, but still widely used [hash function](/wiki/Hash_function "Hash function") which takes an input and produces a 160-[bit](/wiki/Bit "Bit") (20-[byte](/wiki/Byte "Byte")) hash value known as a [message digest](/wiki/Message_digest "Message digest") – typically rendered as a [hexadecimal](/wiki/Hexadecimal "Hexadecimal") number, 40 digits long. It was designed by the United States [National Security Agency](/wiki/National_Security_Agency "National Security Agency"), and is a U.S. [Federal Information Processing Standard](/wiki/Federal_Information_Processing_Standard "Federal Information Processing Standard").

Since 2005, SHA-1 has not been considered secure against well-funded opponents; as of 2010 many organizations have recommended its replacement. [NIST](/wiki/NIST "NIST") formally deprecated use of SHA-1 in 2011 and disallowed its use for digital signatures in 2013. As of 2020, [chosen-prefix attacks](/wiki/Chosen-prefix_attack "Chosen-prefix attack") against SHA-1 are practical. As such, it is recommended to remove SHA-1 from products as soon as possible and instead use [SHA-2](/wiki/SHA-2 "SHA-2") or [SHA-3](/wiki/SHA-3 "SHA-3"). Replacing SHA-1 is urgent where it is used for [digital signatures](/wiki/Digital_signatures "Digital signatures").

All major [web browser](/wiki/Web_browser "Web browser") vendors ceased acceptance of SHA-1 [SSL certificates](/wiki/SSL_certificate "SSL certificate") in 2017. In February 2017, [CWI Amsterdam](/wiki/CWI_Amsterdam "CWI Amsterdam") and [Google](/wiki/Google "Google") announced they had performed a [collision attack](/wiki/Collision_attack "Collision attack") against SHA-1, publishing two dissimilar PDF files which produced the same SHA-1 hash. However, SHA-1 is still secure for [HMAC](/wiki/HMAC "HMAC").
Microsoft has discontinued SHA-1 code signing support for Windows Update on August 7, 2020.

SHA-2
---

**SHA-2** (**Secure Hash Algorithm 2**) is a set of [cryptographic hash functions](/wiki/Cryptographic_hash_function "Cryptographic hash function") designed by the United States [National Security Agency](/wiki/National_Security_Agency "National Security Agency") (NSA) and first published in 2001. They are built using the [Merkle–Damgård construction](/wiki/Merkle%E2%80%93Damg%C3%A5rd_construction "Merkle–Damgård construction"), from a [one-way compression function](/wiki/One-way_compression_function "One-way compression function") itself built using the [Davies–Meyer structure](/wiki/One-way_compression_function#Davies–Meyer "One-way compression function") from a specialized [block cipher](/wiki/Block_cipher "Block cipher").

SHA-2 includes significant changes from its predecessor, [SHA-1](/wiki/SHA-1 "SHA-1"). The SHA-2 family consists of six hash functions with [digests](/wiki/Cryptographic_hash_function#message_digest "Cryptographic hash function") (hash values) that are 224, 256, 384 or 512 bits: **SHA-224, SHA-256, SHA-384, SHA-512, SHA-512/224, SHA-512/256**. SHA-256 and SHA-512 are novel hash functions computed with eight 32-bit and 64-bit words, respectively. They use different shift amounts and additive constants, but their structures are otherwise virtually identical, differing only in the number of rounds. SHA-224 and SHA-384 are truncated versions of SHA-256 and SHA-512 respectively, computed with different initial values. SHA-512/224 and SHA-512/256 are also truncated versions of SHA-512, but the initial values are generated using the method described in [Federal Information Processing Standards](/wiki/Federal_Information_Processing_Standards "Federal Information Processing Standards") (FIPS) PUB 180-4.

SHA-2 was first published by the [National Institute of Standards and Technology](/wiki/National_Institute_of_Standards_and_Technology "National Institute of Standards and Technology") (NIST) as a U.S. federal standard (FIPS). The SHA-2 family of algorithms are patented in US patent 6829355. The United States has released the patent under a [royalty-free](/wiki/Royalty-free "Royalty-free") license.

As of 2011, the best public attacks break [preimage resistance](/wiki/Preimage_attack "Preimage attack") for 52 out of 64 rounds of SHA-256 or 57 out of 80 rounds of SHA-512, and [collision resistance](/wiki/Collision_attack "Collision attack") for 46 out of 64 rounds of SHA-256.

SHA-3
---

**SHA-3** (**Secure Hash Algorithm 3**) is the latest member of the [Secure Hash Algorithm](/wiki/Secure_Hash_Algorithm "Secure Hash Algorithm") family of standards, released by [NIST](/wiki/NIST "NIST") on August 5, 2015. Although part of the same series of standards, SHA-3 is internally different from the [MD5](/wiki/MD5 "MD5")-like [structure](/wiki/Davies-Meyer "Davies-Meyer") of [SHA-1](/wiki/SHA-1 "SHA-1") and [SHA-2](/wiki/SHA-2 "SHA-2").

SHA-3 is a subset of the broader cryptographic primitive family **Keccak** ([/ˈkɛtʃæk/](/wiki/Help:IPA/English "Help:IPA/English") or [/ˈkɛtʃɑːk/](/wiki/Help:IPA/English "Help:IPA/English")), designed by [Guido Bertoni](/w/index.php?title=Guido_Bertoni&action=edit&redlink=1 "Guido Bertoni (page does not exist)"), [Joan Daemen](/wiki/Joan_Daemen "Joan Daemen"), Michaël Peeters, and [Gilles Van Assche](/wiki/Gilles_Van_Assche "Gilles Van Assche"), building upon [RadioGatún](/wiki/RadioGat%C3%BAn "RadioGatún"). Keccak's authors have proposed additional uses for the function, not (yet) standardized by NIST, including a [stream cipher](/wiki/Stream_cipher "Stream cipher"), an [authenticated encryption](/wiki/Authenticated_encryption "Authenticated encryption") system, a "tree" hashing scheme for faster hashing on certain architectures, and [AEAD](/wiki/AEAD "AEAD") ciphers Keyak and Ketje.

Keccak is based on a novel approach called [sponge construction](/wiki/Sponge_function "Sponge function"). Sponge construction is based on a wide random function or random [permutation](/wiki/Block_cipher "Block cipher"), and allows inputting ("absorbing" in sponge terminology) any amount of data, and outputting ("squeezing") any amount of data, while acting as a pseudorandom function with regard to all previous inputs. This leads to great flexibility.

NIST does not currently plan to withdraw SHA-2 or remove it from the revised Secure Hash Standard. The purpose of SHA-3 is that it can be directly substituted for SHA-2 in current applications if necessary, and to significantly improve the robustness of NIST's overall hash algorithm toolkit.

The creators of the Keccak algorithms and the SHA-3 functions suggest using the faster function [KangarooTwelve](#Later_developments) with adjusted parameters and a new tree hashing mode without extra overhead for small message sizes.