# Xper

Welcome to the HyperSDK Local VM Management project! This repository is dedicated to simplifying the creation and management of local virtual machines using HyperSDK and the Go programming language.

## Description

HyperSDK Local VM Management is designed to streamline the process of setting up and running virtual machines on your local environment. With a focus on simplicity and efficiency, this project leverages the power of HyperSDK and the flexibility of Go to provide a seamless experience for developers and system administrators.

### Getting Started

To create a new VM, first run 

```
go mod tidy 
```

and then move to the consts/consts.go file and change thr HRP values there, then

in the terminal run the command 

```
export PATH=$PATH:$(go env GOPATH)/bin
```

to set the default path

then run 

```
MODE="run-single" ./scripts/run.sh
```

followed by 

```
./scripts/build.sh
```

to get your local VM running.

### Interacting with the VM

You can run commands like 

```
./build/token-cli action create-asset
```

to create your own token 

```
database: .token-cli
address: token1rvzhmceq997zntgvravfagsks6w0ryud3rylh4cdvayry0dl97nsjzf3yp
chainID: Em2pZtHr7rDCzii43an2bBi1M2mTFyLN33QP1Xfjy7BcWtaH9
metadata (can be changed later): MarioCoin
continue (y/n): y
✅ txID: 27grFs9vE2YP9kwLM5hQJGLDvqEY9ii71zzdoRHNGC4Appavug
```

and to mint it 

```
./build/token-cli action mint-asset
```

which will promt a message on the terminal window like 

```
database: .token-cli
address: token1rvzhmceq997zntgvravfagsks6w0ryud3rylh4cdvayry0dl97nsjzf3yp
chainID: Em2pZtHr7rDCzii43an2bBi1M2mTFyLN33QP1Xfjy7BcWtaH9
assetID: 27grFs9vE2YP9kwLM5hQJGLDvqEY9ii71zzdoRHNGC4Appavug
metadata: MarioCoin supply: 0
recipient: token1rvzhmceq997zntgvravfagsks6w0ryud3rylh4cdvayry0dl97nsjzf3yp
amount: 10000
continue (y/n): y
✅ txID: X1E5CVFgFFgniFyWcj5wweGg66TyzjK2bMWWTzFwJcwFYkF72
```

and then you can check your balance using 

```
./build/token-cli key balance
```

when you are done, your output should be something like this

```
database: .token-cli
address: token1rvzhmceq997zntgvravfagsks6w0ryud3rylh4cdvayry0dl97nsjzf3yp
chainID: Em2pZtHr7rDCzii43an2bBi1M2mTFyLN33QP1Xfjy7BcWtaH9
assetID (use TKN for native token): 27grFs9vE2YP9kwLM5hQJGLDvqEY9ii71zzdoRHNGC4Appavug
metadata: MarioCoin supply: 10000 warp: false
balance: 10000 27grFs9vE2YP9kwLM5hQJGLDvqEY9ii71zzdoRHNGC4Appavug
```

### Authors

Parth Verma

