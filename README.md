## Proxy Upgradable Contracts
This is an implementation of upgradable smart contract using proxies

## Overview:

## How to Use:

### Installation & Setup:

1. Installing Brownie: Brownie is a python framework for smart contracts development,testing and deployments. It's quit like [HardHat](https://hardhat.org) but it uses python for writing test and deployements scripts instead of javascript.
   Here is a simple way to install brownie.
   ```
    pip install --user pipx
    pipx ensurepath
    # restart your terminal
    pipx install eth-brownie
   ```
   Or if you can't get pipx to work, via pip (it's recommended to use pipx)
    ```
    pip install eth-brownie
    ```
   
3. Clone the repo:
   ```sh
   git clone https://github.com/Aymen1001/proxy_upgradable_contracts.git
   cd proxy_upgradable_contracts
   ```

4. Set your environment variables:

   To be able to deploy to real testnets you need to add your PRIVATE_KEY (You can find your PRIVATE_KEY from your ethereum wallet like metamask) and the infura project Id (just create an infura account it's free) to the .env file:
   ```
   PRIVATE_KEY=<PRIVATE_KEY>
   WEB3_INFURA_PROJECT_ID=<< YOUR INFURA PROJECT ID >>
   ```
### How to run:

To upgrade the Box contract to BoxV2 on development network, run the command :
   ```sh
   brownie run scripts/upgrade_box_contract.py
   ```
To use upgrade on real testnets (kovan, rinkbey,...), run the command :
   ```sh
   brownie run scripts/upgrade_box_contract.py --network=<testnet name>
   ```
### Testing:

The tests for the upgrade functionnalities can be found in the tests folder. 

You can run all the tests by :
   ```sh
   brownie test
   ```
Or you can test each function individualy:
   ```sh
   brownie test -k <function name>
   ```
