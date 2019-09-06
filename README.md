# gostenginessl
https://github.com/gost-engine/engine compiled Gost 2012 engine OpenSSL compiled for Windows 32

Use it with Win32 OpenSSL v1.1.1c https://slproweb.com/products/Win32OpenSSL.html

add gost.dll to the bin dir of OpenSSL

at the start of openssl.cfg add:
openssl_conf = openssl_def

at the end openssl.cfg add:
[openssl_def]
engines = engine_section

[engine_section]
gost = gost_section

[gost_section]
engine_id = gost
dynamic_path = ./gost.dll
default_algorithms = ALL
CRYPT_PARAMS = id-Gost28147-89-CryptoPro-A-ParamSet
