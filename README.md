# Checksum-Wallet
Wallet checksums
[![Build Status](https://travis-ci.org/blockchain/blockchain-wallet-v4-frontend.svg?branch=master)](https://travis-ci.org/blockchain/blockchain-wallet-v4-frontend)
[![Coverage Status](https://coveralls.io/repos/github/blockchain/blockchain-wallet-v4-frontend/badge.svg?branch=development)](https://coveralls.io/github/blockchain/blockchain-wallet-v4-frontend?branch=development)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)

# Blockchain Wallet v4
Be Your Own Bank at [blockchain.info/wallet](https://blockchain.info/wallet).
Please [contact support](https://support.blockchain.com) if you have any issues using the wallet.

## About
This repo contains the three codebases/packages listed below.

### Packages
 * [blockchain-info-components](./packages/blockchain-info-components) The shared UI components library.
 * [blockchain-wallet-v4](./packages/blockchain-wallet-v4) The functional library for handling wallets.
 * [blockchain-wallet-v4-frontend](./packages/blockchain-wallet-v4-frontend) The frontend application built with React/Redux.


## Local Development
1. Ensure Node version >= 10.2 and NPM version >= 6 are installed
2. Run the following command to install necessary global packages: `npm install -g yarn babel-cli rimraf cross-env`
3. Install, link and hoist packages: `yarn`
4. Start the application in development mode: `yarn start`
5. The frontend application will now be accessible via browser at `localhost:8080`

If you require the application to run locally over HTTPS, follow the instructions [here](./config/ssl/ssl.md).

### Windows Support
To ensure proper support for Windows, please take the following actions before running the above setup instructions.
1. Open a Powershell window with rights elevated to an Administrator.
2. Run `npm install -g windows-build-tools`. This will install Python 2.7 and Visual C++ Build Tools which are required to compile some native Node modules.
3. Ensure Python has been added to your environment variables by opening a cmd prompt and typing `python`. If you get a `CommandNotFoundException` message, add the folder `%USERPROFILE%\.windows-build-tools\python27` to your environment variables.

### Tips & Useful Commands
1. To completely remove all dependencies and artifacts run `yarn clean`
2. To add/remove an NPM package run `yarn add` or `yarn remove` in the package folder. After installing or uninstalling a NPM package, run `yarn` in the root folder to re-init the project
3. All development specific dependencies should be installed as a `dev-dependency` in the top level `package.json` via `yarn i --save-dev [package-name]`
4. All application specific dependencies should be installed in the specific packages `package.json` via `yarn i --save [package-name]`

### Running Environments Locally
The frontend application can be ran locally with different build configurations found in `config/env`.  The following commands are available:
 * `yarn start` Runs the application with the `development.js` configuration file
 * `yarn start:dev` Runs the application with the `development.js` configuration file
 * `yarn start:staging` Runs the application with the `staging.js` configuration file
 * `yarn start:testnet` Runs the application with the `testnet.js` configuration file
 * `yarn start:prod` Runs the application with the `production.js` configuration file
 * `yarn run:prod` Runs the application mimicking the production environment entirely (i.e. code is bundled and minified, HMR is disabled,
  Express server is used (`./server.js`) and the `production.js` configuration file is loaded)

Notes:
 * Developers will need to manually create the `development.js` and `staging.js` files
 * Custom application runtimes are possible by modifying the corresponding environment files found in the `config/env` folder
 
### Useful Chrome Extensions 
