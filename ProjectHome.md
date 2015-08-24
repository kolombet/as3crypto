As3 Crypto is a cryptography library written in Actionscript 3 that provides several common algorithms. This version also introduces a TLS engine (TLS is commonly known as SSL.)

  * Protocols: TLS 1.0 support (partial)
  * Certificates: X.509 Certificate parsing and validation, built-in Root CAs.
  * Public Key Encryption: RSA (encrypt/decrypt, sign/verify)
  * Secret Key Encryption: AES, DES, 3DES, BlowFish, XTEA, RC4
  * Confidentiality Modes: ECB, CBC, CFB, CFB8, OFB, CTR
  * Hashing Algorithms: MD2, MD5, SHA-1, SHA-224, SHA-256
  * Paddings available: PKCS#5, PKCS#1 type 1 and 2
  * Other Useful Stuff: HMAC, Random, TLS-PRF, some ASN-1/DER parsing

The library is offered under the BSD license, and include several derivative works from Java, C and javascript sources. Check the [LICENSE.txt](http://as3crypto.googlecode.com/svn/trunk/as3crypto/LICENSE.txt) file for a list of contributors.

You can look at [a demo](http://crypto.hurlant.com/demo/) of the functionality of the library. It's built with Flex 2. It includes a unit test tab, and a benchmark tab.

This is what the benchmark tab outputs on my computer (Athlon64 2Ghz):
```
The 'numbers' are in 1000s of bytes per second processed.
type             16 bytes     64 bytes    256 bytes   1024 bytes   8192 bytes
md2                  1.01k        3.64k       15.08k       53.89k      171.76k
md5                221.85k      447.32k      739.54k      893.72k      905.82k
sha1                82.28k      184.78k      286.76k      336.03k      345.41k
sha224              60.84k      125.67k      200.27k      234.28k      247.58k
sha256              60.52k      126.30k      199.19k      234.04k      246.01k
hmac-md5            48.37k      159.37k      282.87k      295.15k      341.21k
hmac-sha1           18.29k       64.82k      165.72k      277.60k      342.52k
hmac-sha224          5.75k       24.84k      125.71k      204.35k      256.36k
hmac-sha256         15.10k       49.33k      123.71k      206.17k      249.08k
rc4                117.24k      381.34k      878.93k     1315.01k     1539.44k
xtea-cbc             2.49k        6.48k       12.80k       33.00k       44.48k
aes128-cbc           1.61k        4.01k       22.97k       78.55k      205.01k
aes192-cbc           1.34k        5.13k       20.91k       69.45k      172.43k
aes256-cbc           1.48k        5.63k       18.87k       63.45k      150.39k
blowfish-cbc         2.77k       10.81k       42.28k      140.27k      343.05k
des-cbc              2.53k        9.73k       35.20k      124.84k      624.88k
3des-cbc             2.50k        9.72k       35.61k      115.21k      253.42k
```
The library has not been optimized for speed, and those numbers could probably be improved.

You can [browse the source](http://crypto.hurlant.com/demo/srcview/), [download the source](http://as3crypto.googlecode.com/files/Crypto.zip) or [download the SWC binary](http://as3crypto.googlecode.com/files/as3crypto.swc)

Check out the [release notes](http://as3crypto.googlecode.com/svn/trunk/as3crypto/RELEASENOTES.txt) for a bit more details.

Things that should make it in the next release:
  * better ASN-1 parsing
  * SSL 3.0 support
  * various bugfixes (Socket, BigInteger)