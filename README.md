<img width="1200" alt="Labs" src="https://user-images.githubusercontent.com/99700157/213291931-5a822628-5b8a-4768-980d-65f324985d32.png">

<p>
 <h3 align="center">Chainstack is the leading suite of services connecting developers with Web3 infrastructure</h3>
</p>

<p align="center">
  <a target="_blank" href="https://chainstack.com/build-better-with-ethereum/"><img src="https://github.com/soos3d/blockchain-badges/blob/main/protocols_badges/Ethereum.svg" /></a>&nbsp;  
  <a target="_blank" href="https://chainstack.com/build-better-with-bnb-smart-chain/"><img src="https://github.com/soos3d/blockchain-badges/blob/main/protocols_badges/BNB.svg" /></a>&nbsp;
  <a target="_blank" href="https://chainstack.com/build-better-with-polygon/"><img src="https://github.com/soos3d/blockchain-badges/blob/main/protocols_badges/Polygon.svg" /></a>&nbsp;
  <a target="_blank" href="https://chainstack.com/build-better-with-avalanche/"><img src="https://github.com/soos3d/blockchain-badges/blob/main/protocols_badges/Avalanche.svg" /></a>&nbsp;
  <a target="_blank" href="https://chainstack.com/build-better-with-solana/"><img src="https://github.com/soos3d/blockchain-badges/blob/main/protocols_badges/Solana.svg" /></a>&nbsp;
</p>

<p align="center">
  <a target="_blank" href="https://chainstack.com/protocols/">Supported protocols</a> •
  <a target="_blank" href="https://chainstack.com/blog/">Chainstack blog</a> •
  <a target="_blank" href="https://docs.chainstack.com/">Chainstack docs</a> •
  <a target="_blank" href="https://docs.chainstack.com/api/">Blockchain API reference</a> •
  <a target="_blank" href="https://console.chainstack.com/user/account/create">Start for free</a>
</p>

# Ape Chainstack Plugin

Chainstack network provider plugins.

This plugin allows using the Ape framework with Chainstack as a node provider in an easy and integrated way.

Ape is an innovative smart contract development and testing framework.
It is inspired by Brownie, and it has essentially the same syntax.
Still, Ape focuses on a more modular approach, allowing us to build and use external plugins to add functionality.

## Quick start

See [Smart contracts framework Ape by ApeWorX—What is it and how to use it](https://chainstack.com/apeworx-ape-framework-what-is-it-and-how-to-use-it/) to learn how to create an Ape project and use the Chainstack plugin to deploy it.

Follow these steps to sign up on Chainstack, deploy a node, and find your endpoint credentials:

1. [Sign up with Chainstack](https://console.chainstack.com/user/account/create).
1. [Deploy a node](https://docs.chainstack.com/platform/join-a-public-network).
1. [View node access and credentials](https://docs.chainstack.com/platform/view-node-access-and-credentials).

> **Note:** At this moment only the Ethereum network is supported.

After [installation](#installation):

Create an environment variable with your Chainstack node URL in this format `CHAINSTACK_"NETWORK"_URL=ENDPOINT_URL`; for example:

```sh
export CHAINSTACK_GOERLI_URL=https://nd-11X-26X-16X.p2pify.com/YOUR_API_KEY
```

Use the command `ape networks list` to see the networks available:

```sh
ethereum  (default)
├── mainnet
│   ├── geth  (default)
│   └── chainstack
├── ropsten
│   ├── geth  (default)
│   └── chainstack
├── kovan
│   └── geth  (default)
├── rinkeby
│   ├── geth  (default)
│   └── chainstack
├── goerli
│   ├── geth  (default)
│   └── chainstack
└── local  (default)
    ├── geth
    └── test  (default)
```

Use the `--network` command to access the console using your node; for example:

```bash
ape console --network ethereum:goerli:chainstack
```

Check the Ape docs to see [how to select a network](https://docs.apeworx.io/ape/stable/userguides/networks.html).

Now you are ready to use Ape to develop and test your smart contract, checkout the [Ape Academy](https://academy.apeworx.io/) for tutorials.

## Requirements

- Linux or macOS
- Windows Subsystem Linux ([WSL](https://docs.microsoft.com/en-us/windows/wsl/install)) if operating on windows.

### Dependencies

- [python3](https://www.python.org/downloads) version 3.7.2 or greater
- [Ape framework](https://github.com/ApeWorX/ape)
- python3-dev

  - MacOS. Should already have the [correct headers if Python is installed with `brew`](https://stackoverflow.com/questions/32578106/how-to-install-python-devel-in-mac-os)

  - Linux. Install python3-dev with:

  ```sh
  sudo apt-get install python3-dev
  ```

> **Note:** Always check the [Ape docs to find the updated requirements](https://docs.apeworx.io/ape/stable/userguides/quickstart.html#prerequisite).

## Installation

### Virtual environment

It is recommended to operate in a virtual environment; you will need to [install Ape](https://github.com/ApeWorX/ape#installation) in the virtual environment if you decide to use one.

### Install ape-chainstack via `pip`

You can install the latest release via [`pip`](https://pypi.org/project/pip/):

```bash
pip install ape-chainstack
```

### Install ape-chainstack via `setuptools`

You can clone the repository and use [`setuptools`](https://github.com/pypa/setuptools) for the most up-to-date version:

```bash
git clone https://github.com/ApeWorX/ape-chainstack.git
cd ape-chainstack
python3 setup.py install
```

Verify that the Chainstack plugin was installed correctly with this command:

```bash
ape plugins list
```

It will show a list of all the plugins installed, and Chainstack will be there.

```bash
Installed Plugins:
  chainstack    <current version number>
```

## Development

This project is in development and should be considered a beta.
Things might not be in their final state and breaking changes may occur.
Comments, questions, criticisms and pull requests are welcomed.

## License

This project is licensed under the [Apache 2.0](LICENSE).
