# ethersapp 
[ethersapp](https://yuetloo.github.io/ethersapp/) is an open source, javascript, client-side tool for exploring the Ethereum smart contracts on testnet and mainnet.  For testnet, the contract ABI is maintained in the js/abi.js file.  For mainnet, the ABI is retrieved from [etherchain.org](https://etherchain.org) API

# Purpose
ethersapp was created to help me learn about ethereum contracts.  I was inspired to create this tool after attending a few ethereum contract introduction meetup sessions by [Ledger Labs] (https://ledgerlabs.io).

# Security
Please note that ethersapp has not been through a comprehensive security review. It is an experimental software intended for small amount of Ether to be used to experiment with Ethereum smart contracts. Only functions in a smart contract that require a transaction require Ether to run.  Constant functions labeled with a **"C"** beside the function name do not require Ether to run.

# Usage
1. Select a network (testnet vs. mainnet) from the dropdown list on the top right corner of the page

2. Select or enter the contract address to search for a contract

   For testnet, you can add or delete contract ABI from the dropdown list. There are 3 defalt ABI and they cannot be deleted.
   For mainnet, you can get the list of contracts with source and ABI from [https://etherchain.org/contracts](https://etherchain.org/contracts).

3. Select a function to work with from the left hand side panel 

4. Fill in function input parameter values

5. Fill in 'Sender Address'

   'Sender Address' is optional for constant functions. You can manually enter the 'Sender Address' value in the input box for constant functions. For non-constant (transactional) functions, you must click the 'Wallet' button to import a wallet with private key and the 'Sender Address' will be populated automatically.

   Currently, you can only import the file containing Geth JSON V3 format.  You can generate the wallet file using Geth or [https://ethereumwallet.com](https://ethereumwallet.com).

   The following fields will be populated automatically with value from etherscan.io:
   * Balance - this field is for information only, it is not sent in the transaction
               For testnet, the 'Add More' button will be available to request more Ether from Parity: http://icarus.parity.io/rain/{your_address}

   * Nonce - this is auto populated from etherscan.io
   * Gas Price - this is auto populated from [etherchain] (https://etherchain.org/api/gasPrice)  
   * Gas Limit - this is auto populated with a hardcoded value of 500000
   
6. Value to Send
   Fill in this field only if you want to send Ether (in Wei) to the contract

7. Click the 'Call Function' or 'Send Transaction' button to run the function


# License
MIT License.

# Contribution
Contribution is welcomed at the following Ethereum address:

`0xdeabfa77c044107d78128baba8beee8380d833e4`
