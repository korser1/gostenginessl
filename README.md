# gostenginessl
Gost 2012 engine OpenSSL compiled for Windows 32


Use it with Openssl 1.1.0g https://slproweb.com/products/Win32OpenSSL.html

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
