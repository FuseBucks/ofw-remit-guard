# OFW Remit Guard

Smart contracts (Foundry + OpenZeppelin) and a Python agent for OFW remittances.

## Project structure

```
contracts/   Solidity contracts, tests and scripts (Foundry)
agent/       Python agent
```

## Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation)
- Python 3.14+
- Git

## Setup

Clone with submodules (OpenZeppelin and forge-std live in `contracts/lib`):

```bash
git clone --recursive https://github.com/FuseBucks/ofw-remit-guard.git
cd ofw-remit-guard
```

Already cloned without `--recursive`? Run:

```bash
git submodule update --init --recursive
```

### Contracts

```bash
cd contracts
forge build
forge test
```

### Agent

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r agent/requirements.txt
```

## Environment variables

Secrets go in a `.env` file, which is gitignored. Never commit private keys or API keys.
