# OpenSSL with Rocca-S 
## About
This is a fork of [OpenSSL](https://www.openssl.org/) to suport Rocca-S.
The original README file of OpenSSL can be found at README-OpenSSL.md

Rocca-S is a symmetric encryption algorithm with high throughput.
Detail of Rocca-S algorithm can be found in the following Internet Draft:

https://datatracker.ietf.org/doc/draft-nakano-rocca-s/

## Support Architecture
This software only suport the following architecture:

- SIMD
- x86-64 architecture (with AES-NI support)

## Build and test
Folloiwng depencencies should be installed to build this software:

- make
- gcc
- libc-dev

After installing the required software, you can build this software with the following commands:

```
./Configure no-shared
make
```

Then, you can test the software. The following command shows the list of supported ciphers and Rocca-S should be listed.

```
cd apps
./openssl ciphers -v
```

Other testing method provided by OpenSSL can be used as well and Rocca-S can be used as one of the cipher algorithms.

# License
The source code is provided under the Apache License 2.0.
The full text is included in the file LICENSE.txt.
