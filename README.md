## --> Binance Smart Chain only <--

# About
This repo intends to maintain up to date the list of projects with its MasterChef address in a JSON. Additional information can also be provided in the json, to serve any other purpose.

The MasterChef is the entrypoint Smart Contract to manage all the pools of a DeFi/Farming project. Starting from the MasterChef Smart Contract, all the information of the projects can be deducted and even calculated (token, pools, TVL, APR/APY, ...). But this is not the purpose of that repository.

# Adding / Updating a project
Create a PR with the new file or the modifications needed. The mods will review it and merge it after.
Set draft label for PR not to be merged immediately.

# File specifications
Each Project has one JSON file, to prevent git conflicts.

## Files location
The JSON files MUST be in the /list directory

## File name
The filename of the JSON file:
- SHOULD be the name of the project. The not-slugified project name can be set in the file, under the key `name`
- MUST be slugified

## File structure
Each JSON file in the /list folder MUST be structured as follows.

The address MUST be filled in and checksum compliant.

The other keys SHOULD be filled in.

```json
{
  "address": "0x123456789abcdef123456abcdef123456789abc",
  "name": "Acme Swap",
  "website_url": "https://www.acme-swap.finance",
  "logo_url": "https://www.acme-swap.finance/logo.svg",
  "app_url": "https://app.acme-swap.finance",
  "medium_url": "https://acme-swap.medium.com",
  "twitter_url": "https://twitter.com/acme-swap",
  "telegram_url": "http://t.me/acme-swap",
  "github": "https://github.com/acme-swap"
}
```

# Todo
- [ ] Serve JSON Data from Github Pages
- [ ] Screen for new MasterChef contract that pops up the BSC
- [ ] CI: Setup a JSON linter on PR submission
- [ ] CI: Setup a specification checker on PR submission
- [ ] CI: Check that address is a MasterChef address
