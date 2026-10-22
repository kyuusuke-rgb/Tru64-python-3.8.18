```
===================================================================
Python 3.8.18 for Tru64 UNIX (OSF/1 5.1b) - Binary Package
Target: alphaev56-dec-osf5.1b
===================================================================

1. DESCRIPTION
   This package contains Python 3.8.18 built natively on Tru64 UNIX v5.1b
   (DEC Alpha EV56) using GCC 4.7.4 with 64-bit support.
   To circumvent OSF/1 dynamic linking (dlopen) constraints, key C-extensions 
   are statically embedded into the main binary.

   Statically built-in modules include:
    - _ssl (OpenSSL 1.1.1), hashlib (md5, sha1, sha256, sha512, sha3, blake2)
    - zlib
    - _socket, select
    - _json, _csv, _struct
    - _datetime, _pickle, _asyncio
    - math, cmath, unicodedata, etc.

2. EXTRACT & INSTALL
   Run the following commands as root to extract to /usr/local:

     # cd /usr/local
     # gzip -dc /path/to/Tru64_Python_3.8.18_static.tar.gz | /sbin/tar xvf -

3. ENVIRONMENT SETUP (.profile)
   Add the following lines to ensure /usr/local precedes system paths:

     export PATH=/usr/local/bin:$PATH
     export LD_LIBRARY_PATH=/usr/local/lib:/usr/local/ssl/lib:$LD_LIBRARY_PATH

4. VERIFICATION
   Test the installation using:

     # /usr/local/bin/python3 -V
     # /usr/local/bin/python3 -c "import math, json, datetime, ssl, hashlib; print('Python 3.8 on Tru64 works!')"
===================================================================
```
