# REKT Wallet

REKT Wallet is a fork of the Avalanche wallet originally found at `wallet.avax.network`

It's supposed to run as a standalone app using [Electron](https://www.electronjs.org/pt/)

I wanted a wallet that was hosted in my PC and ran outside web browsers, in a clean environment free of extensions, malware, spyware and away from trackers, analytics, spyware and other security hazards.

While technically Electron *is* a web browser, it is a barebones one which is not ideal for browsing. Therefore the odds of finding malware, spyware, trackers and other security risks on it are significantly lower than in a typical general-purpose web browser.

For example, REKT Wallet can't be loaded from a malicious web link found on social media. It can only run from your hard drive, upon your command.

The github history is open for anyone to audit. So if you clone the repo from github and run it cleanly, odds are this is one of the most secure wallets available for Avalanche.

But don't trust, verify. Check the code out, view the diffs, DYOR until you are confident that this is safe to use. Don't take my word for it.

## Building REKT Wallet

Follow the original instructions for the original Avalanche Wallet below

## Running REKT

`yarn electron:serve`

## Differences from Avalanche Wallet 

The core application is the original Vue-based Avalanche Wallet running inside Electron. It gets embedded in an Electron window from within your own local computer. The entire app is hosted in your local computer. 

Unlike the original Avalanche Wallet, there is no web connection made in order to load the code (it's on your hard drive). After it is loaded, the only network connections made are to official Avalanche API endpoints for price update, UTXOs, balances, etc.

Additionally, the following modifications were made :

* Removed all externally-loaded assets (fonts, etc)
* Removed all analytics-related code from the code (user tracking)
* Substituted proprietary fonts for generic ones (Verdana)
* Replaced Ava Labs' legal docs and references with a BSD License

## Privacy Oriented

The wallet only connects to avax.network and Glacier endpoints. No tracking, no external connections of any other kind. I'm cleaning the code as a hobby, so if you find any extraneous internet connection while debugging the app, [please let me know](https://crypto.bi/forum/forums/support/).

The goal is to have a wallet as private as OG Bitcoin wallets from the 2000's

E.g. I removed Google fonts loading as well for this purpose. Nothing should get loaded from external sources. No 3rd party services should get pinged when you run this wallet. 

## Notes

Consider this experimental software.

And remember, I do this as a hobby.


## Contact

[REKT Support Forum](https://crypto.bi/forum/forums/support/)


#### ---- ORIGINAL AVA LABS DOCUCMENTATION BELOW THIS LINE ----

# Avalanche (AVAX) Wallet

This is the frontend Vue.js application for the Avalanche (AVAX) Wallet.

## Prerequisites

-   Yarn (https://classic.yarnpkg.com/en/docs/install/)
-   Recent version of npm (7.4.0)
-   Node v16
-   Gecko, Avalanche client in Golang (https://github.com/ava-labs/avalanchego)

## Installation

1. Clone the repo `git clone https://github.com/ava-labs/avalanche-wallet.git`
2. Go to root of the project `cd avalanche-wallet`
3. Install javascript dependencies with `yarn install`.

## Running The Project

In order for the wallet to work, it needs the Avalanche network to operate on. By default the wallet will connect to the Avalanche mainnet.

1. If you want to connect to a local network, make sure you have installed and able to run a AvlaancheGo node properly.
2. Run the project with hot reloading `yarn serve`

When you go to the website on your browser, you might get a warning saying
"Site is not secure". This is because we are signing our own SSL Certificates. Please ignore and continue to the website.

## Deployment

1.  Compile and minify to have a production ready application with `yarn build`.
2.  Serve from the `/dist` directory.

## Changing the Network

By default the wallet will connect to the Avalanche tmainnet. You can change to another network by clicking the button labeled `TestNet` on the navigation bar and selecting another network, or add a custom network.

## Explorer API

A valid explorer API is required to correctly display balances for Mnemonic and Ledger type wallets.
The wallet uses the Avalanche Explorer API to display wallet transaction history.

WARNING: This history might be out of order and incomplete.

### Firefox and https

Firefox does not allow https requests to localhost. But the Avalanche Wallet uses https by default, so we will need to change this to http. Make this switch by editing the `vue.config.js` file in the root directory and change

```
devServer: {
    https: true
},
```

to

```
devServer: {
    https: false
},
```

and run `yarn serve` to reflect the change.

# Accounts

The wallet can encrypt your private keys into a secure file encrypted by a password.

```json
{
    "accounts": iUserAccountEncrypted[]
}
```

# Language Setting

Saved into local storage as a 2 letter code.

```
"lang": "en"
```

# Dependencies

##### Avalanche Node (https://github.com/ava-labs/avalanchego)

To get utxos and to send transactions.

#### Explorer API Node (https://github.com/ava-labs/ortelius)

To check if an address was used before, and to get activity history.

# Default Connections

The wallet needs to connect to an Avalanche node, and an explorer node to operate properly.

By default, there are two network options to connect to: `Mainnet` and `Fuji`.

##### Mainnet

-   Avalanche API: `https://api.avax.network:443`
-   Explorer API: `https://explorerapi.avax.network`

##### Fuji (Testnet)

-   Avalanche API: `https://api.avax-test.network:443`
-   Explorer API: `https://explorerapi.avax-test.network`

