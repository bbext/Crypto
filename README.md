# Crypto
Port of Oberon A2 cryptography libs for BBCB2

This is port of Oberon A2 cryptography libs from https://gitlab.inf.ethz.ch/felixf/oberon to Black Box Component Builder.
Code converted from Active Oberon to Component Pascal using OberonParser tool https://github.com/hodzanassredin/OberonParser.

Library X25519 is a port of C# library https://github.com/HirbodBehnam/X25519-CSharp.

TLS implementation now supports TLS v1.2. After port it was slightly modified:

	1. added support for modern Elliptic Curve Diffie Hellman key exchange

	2. support for TLS extensions like SNI
	
	3. bug fixes of original code

You can use ciphers and hashes and other classes in your code. But do not use tls implementation directly now. Right way to use TLS is do it like described in CommStreams documentation for TCP protocol, but instead of  CommTCP name use CryptoTLSStream
	
	Also you can find examples in test modules.
	
		CryptoTestBigNumbers	
		CryptoTestCiphers
		CryptoTestDH
		CryptoTestHashes
		CryptoTestHMAC
		CryptoTestRSA
		CryptoTestTLS
		CryptoTestX25519
