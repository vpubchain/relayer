Relayer - Light Weight Node.js app for Relaying Syscoin and Geth
================================================================

This app subscribes "newBlockHeaders" and "sync" from Go-Ethereum
via web3.js.  Then it pushes the data to syscoin via RPC through
`syscoinsetethheaders` and `syscoinsetethstatus`

Requirement
-----------
This repository currently requires node >= v9.5.0 (node >= v12.0.0 recommended) and pkg >= 4.3.1


How to Build
------------
`git clone https://www.github.com/syscoin/relayer`

`npm install`

`npm install pkg -g`

`pkg package.json`

This will produce portable binaries to be used in other systems.

The expected output is
```
> Targets not specified. Assuming:
  node12-linux-x64, node12-macos-x64, node12-win-x64
> Warning Cannot include addon %1 into executable.
  The addon must be distributed with executable as %2.
  /home/syscoin/relayer/node_modules/sha3/build/Release/sha3.node
  path-to-executable/sha3.node
```


How to Use
----------

`relayer -sysrpcuser [username] -sysrpcpw [password] -sysrpcport [port] -ethwsport [port] -gethtestnet [0/1]`
