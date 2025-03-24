# Updating Operating Cost on a Nym Node with nym-cli

Properly configuring cost parameters on a Nym node is essential to ensuring its sustainability and profitability. In this guide, we will walk you through the step-by-step process of setting up these parameters using the `nym-cli` tool.

## Step 1: Download `nym-cli`

To begin, download the `nym-cli` tool from the official Nym repository by running the following command:

```bash
wget https://github.com/nymtech/nym/releases/download/nym-binaries-v2025.5-chokito/nym-cli
```

## Step 2: Update Cost Parameters

To set the operating costs and profit margin for your node, run the following command, replacing `"word word word ..."` with your mnemonic phrase:

```bash
./nym-cli mixnet operators nymnode settings update-cost-parameters \
  --mnemonic "word word word ..." \
  --interval-operating-cost 800000000 \
  --profit-margin-percent 20
```
### Explanation of Parameters:

* `--mnemonic` : Your account’s mnemonic phrase, used for authentication.
* `--interval-operating-cost` : Defines the operating cost per interval (in this case, 400 Nym).
* `--profit-margin-percent` : Sets the profit margin percentage (in this example, 20%).




If you prefer to execute the command in a single line, you can use the following syntax:

```bash
nym-cli mixnet operators nymnode settings update-cost-parameters --mnemonic "" --profit-margin-percent 20 --interval-operating-cost 400000000
```

