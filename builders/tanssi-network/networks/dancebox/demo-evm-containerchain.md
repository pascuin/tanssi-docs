---
title: Demo EVM Tanssi ContainerChain
description: Test our demo EVM Tanssi ContainerChain to discover the capabilities of a fully Ethereum-compatible Appchain deployed through Tanssi in just a few minutes.
---

## Introduction

A demo EVM Tanssi ContainerChain is deployed on Dancebox for testing purposes. Interact with this chain to discover the capabilities of a fully Ethereum-compatible Appchain deployed through Tanssi.

This article includes the endpoints to interact with this demo EVM ContainerChain, some block explorers, and a quick start example.

## Network Endpoints

The demo EVM ContainerChain HTTPS and WSS endpoints are as follows:

=== "HTTPS"

    ```text
    https://fraa-dancebox-3001-rpc.a.dancebox.tanssi.network/
    ```

=== "WSS"

    ```text
    wss://fraa-dancebox-3001-rpc.a.dancebox.tanssi.network/
    ```

## Quick Start {: #quick-start }

You can interact with the EVM ContainerChain using standard Ethereum libraries, like [Ethers.js](/builders/interact/ethereum-api/libraries/ethersjs){target=\_blank}, [Web3.js](/builders/interact/ethereum-api/libraries/web3js){target=\_blank}, and [Web3.py](/builders/interact/ethereum-api/libraries/web3py){target=\_blank}. To quickly get started, you'll need to create a provider connected to the EVM ContainerChain:

=== "Ethers.js"

    ```js
    import { ethers } from "ethers";

    const providerRPC = {
      EvmContainer: {
        name: 'dancebox-evm-container',
        // Insert your RPC URL here
        rpc: 'https://fraa-dancebox-3001-rpc.a.dancebox.tanssi.network', 
        chainId: 5678, // 0x162E in hex,
      },
    };
    const provider = new ethers.JsonRpcProvider(
      providerRPC.EvmContainer.rpc, 
      {
        chainId: providerRPC.EvmContainer.chainId,
        name: providerRPC.EvmContainer.name,
      }
    );
    ```

=== "Web3.js"

    ```js
    const Web3 = require('web3');

    const web3 = new Web3(
      'https://fraa-dancebox-3001-rpc.a.dancebox.tanssi.network'
    );
    ```

=== "Web3.py"

    ```python
    from web3 import Web3

    web3 = Web3(Web3.HTTPProvider('https://fraa-dancebox-3001-rpc.a.dancebox.tanssi.network')) 
    ```

### EVM Container Chain ID {: #chain-id }

The EVM ContainerChain has a [chain ID](https://chainlist.org/chain/5678){target=\_blank} of: `5678`, which is `0x162E` in hex.

### Block Explorers {: #block-explorers }

For the EVM ContainerChain, you can use any of the following explorers:

- Substrate API - on [Polkadot.js Apps](https://polkadot.js.org/apps/?rpc=wss://fraa-dancebox-3001-rpc.a.dancebox.tanssi.network#/explorer){target=\_blank}
- EVM explorer - on [Blockscout](https://3001-blockscout.a.dancebox.tanssi.network/){target=\_blank} or [Expedition](https://tanssi-evmexplorer.netlify.app/){target=\_blank}

