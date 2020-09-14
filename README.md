# libuhttpd([中文](/README_ZH.md))

[1]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=plastic
[2]: /LICENSE
[3]: https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=plastic
[4]: https://github.com/zhaojh329/libuhttpd/pulls
[5]: https://img.shields.io/badge/Issues-welcome-brightgreen.svg?style=plastic
[6]: https://github.com/zhaojh329/libuhttpd/issues/new
[7]: https://img.shields.io/badge/release-3.3.0-blue.svg?style=plastic
[8]: https://github.com/zhaojh329/libuhttpd/releases
[9]: https://travis-ci.org/zhaojh329/libuhttpd.svg?branch=master
[10]: https://travis-ci.org/zhaojh329/libuhttpd

[![license][1]][2]
[![PRs Welcome][3]][4]
[![Issue Welcome][5]][6]
[![Release Version][7]][8]
[![Build Status][9]][10]

[libev]: http://software.schmorp.de/pkg/libev.html
[http-parser]: https://github.com/nodejs/http-parser
[openssl]: https://github.com/openssl/openssl
[mbedtls]: https://github.com/ARMmbed/mbedtls
[wolfssl]: https://github.com/wolfSSL/wolfssl

A very flexible, lightweight and fully asynchronous HTTP server library based on [libev] and [http-parser] for Embedded Linux.

# Features
* Lightweight and fully asynchronous
* Use [libev] as its event backend
* Support HTTPS - OpenSSL, mbedtls and CyaSSl(wolfssl)
* Support plugin
* Flexible - you can easily extend your application to have HTTP/HTTPS services
* Code structure is concise and understandable, also suitable for learning

# Dependencies
* [libev]
* [http-parser] - A parser for HTTP messages written in C
* [mbedtls] - If you choose mbedtls as your SSL backend
* [wolfssl] - If you choose wolfssl as your SSL backend
* [openssl] - If you choose openssl as your SSL backend

# Configure
See which configuration are supported

	~/libuhttpd/$ mkdir build && cd build
	~/libuhttpd/build$ cmake .. -L
	~/libuhttpd/build$ cmake .. -LH

# Build and install

	~/libuhttpd/build$ make && sudo make install

# Run Example	
Run

	~/libuhttpd/build$ ./example/example
	
Then use the command curl or browser to test

	$ curl 'https://127.0.0.1:8000' -v

# Install on OpenWrt
    opkg update
    opkg list | grep libuhttpd
    opkg install libuhttpd-nossl

If the install command fails, you can [compile it yourself](/BUILDOPENWRT.md).

# [Example](/example)

# Contributing
If you would like to help making [libuhttpd](https://github.com/zhaojh329/libuhttpd) better,
see the [CONTRIBUTING.md](https://github.com/zhaojh329/libuhttpd/blob/master/CONTRIBUTING.md) file.

