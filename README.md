# Baron Chain Wallet Registry

The wallet registry for the Baron Chain Blockchain Ecosystem

## Wallet Data

Wallet data contains information needed to allow dApps to associate wallets with chains.

### Features

The 'features' array contains allows a limited set of features to be defined:
- suggest-chain:  referes to an experimental suggest chain feature. E.g., See Keplr's: https://docs.keplr.app/api/suggest-chain.html
- get-supported-chains: a feature that returns a list of chains supported by the wallet.

### Platforms

A platform object is defined by several properties:
- `device`: (desktop, mobile, tablet, other)
- `type`: (application vs extension)
- `platform` (the system on which the software runs): (ios, android, chrome, firefox, otherOS, otherBrowser)

The `install_link` is optional, but is a good way to confirm to users they've found the correct installation. Try to avoid language-specific url parameters in the URL.

### Example

Here is an example wallet entry:

```
{
  "$schema": "../wallet.schema.json",
  "wallet_name": "keplrmobile",
  "pretty_name": "Keplr",
  "website": "https://www.keplr.app/",
  "git_repo": "https://github.com/chainapsis/keplr-wallet",
  "supported_chains": [
    "cosmoshub",
    "osmosis"
  ],
  "features": [
    "suggest_chain",
    "icns"
    "get_supported_chains"
  ],
  "platforms": [
    {
      "device": "mobile",
      "type": "application",
      "platform": "ios",
      "install_link": "apple/app-store.com/cryptowallet",
    },
    {
      "device": "mobile",
      "type": "application",
      "platform": "android",
      "install_link": "google/play-store.com/cryptowallet",
    }
  ]
}
```


---

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
