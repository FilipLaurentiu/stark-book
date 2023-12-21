# Verifying Cairo proofs

Verifying a SHARP Cairo proof on the Starkex contracts is done in a number of transactions:

* 3 Verify Merkle transactions ([example](https://etherscan.io/tx/0x5ad19d4524e0d2f2281dd71b8b1030fca7131ce74b821b936f73df2cba9d65e5))
* 8 Verify FRI transactions ([example](https://etherscan.io/tx/0xccc7446d9e5e14892496ee3956f0e9579c2f56b8e70441623aa283c302130201))
* A bunch of Register Continuous Memory Page ([example](https://etherscan.io/tx/0x6862ef5e0ce7599124e7c81625130990a102f483dde292d76b8d869b7d280ea7))
* A single Verify Proof and Register ([example](https://etherscan.io/tx/0x720571bcac39e6b973537d7dd2ba253072e6f82c634ce361de73769d026ce4a1))

The reason the verification of a proof is split in multiple transactions is because proofs are too large, and the verification cost too much gas, to fit in a single transaction. 

> Note: Proofs can be split using [stark-evm-adapter](https://github.com/zksecurity/stark-evm-adapter/)