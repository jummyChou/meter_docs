# Introduction to Developer Documentation

Verse is DeFi infrastructure with a built-in, crypto-native, metastable currency called MTR. You can use Verse as a Layer 2 blockchain to build DeFi apps on top of, or as a highly-decentralized, high-performance side chain for Ethereum and other public chains.

There are two primary methods of interacting with Verse:

**Ethereum RPC**

In order to better support existing Ethereum dApp developers, we developed an Ethereum emulation mode for Verse. Through an addon module called webgear Meter nodes are able to understand Ethereum transaction format and support the standard Ethereum RPC interface. It is like using the Apple M1 silicon to run x86 applications with a 100x performance improvement. Developers are even able to use their preferred Ethereum development tools like `Remix`, `ethers.js` and `web3.js` to interact with Verse. Due to the limitations of the Ethereum RPC, not all Meter functionality is available in Ethereum emulation mode. In this mode, MTRG must be treated as a special ERC20 token via a system contract.

The other difference between Verse and Ethereum is that Verse removed the sequential nonce concept in Ethereum and uses a random number as nonce instead. The Ethereum emulation layer will automatically generate the random nonce, you will not be able to replace a transaction with the same nonce. Additionally, the sender of a transation must rely on the transaction hash returned by the node instead of generating it directly offline.

When interacting with Verse you must use "Injected Web3" in Remix alongside Metamask.

**Testnet:**

Warringstakes Testnet Endpoints:

RPC:[ ](https://test-rpc0.stp.network)[https://test-rpc0.stp.network](https://test-rpc0.stp.network)

ChainID: 72

Currency Symbol:   STPT

Explorer:[ ](https://testnet-explorer.stp.network)[https://testnet-explorer.stp.network/](https://testnet-explorer.stp.network)

_ERC20 System Interface:_

MTRG: 0x8a419ef4941355476cf04933e90bf3bbf2f73814

MTR: 0x4cb6cef87d8cadf966b455e8bd58fff32aba49d1

***

**Currently, there is a limitation that MTR and MTRG could only be sent to a contract address through smart contract interactions. For example, if you want to send MTR to a contract address manually, you will have to use the above ERC20 system interface.**

Faucet for Testnet can be found at:

{% embed url="http://faucet-warringstakes.meter.io" %}

**Source Code Verification**

Verse explorer uses [Sourcify](https://github.com/ethereum/sourcify) for verifying the onchain contracts' byte code is exactly the same as the source code. Verifying contracts also allows the explorer to properly decode smart contract transactions. There are various tools (for example Remix plugins) that help developers to verify on Sourcify.

The submission for source code can be either done through[ Verse  Explorer](https://testnet-explorer.stp.network) or [Sourcify Portal](https://sourcify.dev). There are two levels of verification: 1. source code match and 2. both source code, metadata match. Source code match is considered the minimum for contract verification purposes.

**RESTful API (Not Required if you are using Ethereum RPC toolchains)**
