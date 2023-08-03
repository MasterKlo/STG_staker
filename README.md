# Polygon STG Staker

This Python script is designed to automate certain operations involving the Polygon STG token. The script interacts with the Polygon blockchain using the `web3` library to perform tasks such as approving spending and creating locks for the STG token.

## Features

### 1. Approve Spending

The script facilitates the approval of spending for a specific amount of STG tokens from multiple wallets. This is achieved through the `approve` function, which approves a designated spender to spend a given amount of STG tokens from a wallet. The approved amount is specified in the `amount_to_approve` variable.

### 2. Create Lock

The script also offers the ability to create locks for STG tokens. The `create_lock` function allows users to lock a certain amount of STG tokens for a specified duration. This is useful for participating in token staking or other time-bound activities. The lock amount and unlock time are determined by the `valuem` and `unlock_time` variables, respectively.

### 3. Gas Price Monitoring

To ensure cost-effectiveness, the script continually monitors the current gas price on the Polygon network. It waits for the gas price to drop below a certain threshold (200 Gwei) using the `wait_for_low_gas_price` function before proceeding with transactions.

## Configuration

The script reads private keys from the "private_keys.txt" file, each representing a different wallet. It processes each wallet by performing the following steps:

1. Retrieves the STG token balance for the wallet.
2. Approves spending for a specified spender address.
3. Creates a lock for a portion of the wallet's STG tokens.
4. Adds a random delay between wallet processing to avoid overwhelming the network.

## Prerequisites

- Python 3.x
- pip install -r requirements.txt

## How to Use

1. Prepare a "private_keys.txt" file containing the private keys of the wallets you want to process.
2. Ensure that the `STG_abi.json` and `loke_abi.json` files are available, containing the ABIs for the STG and Loke contracts, respectively.
3. Modify the `spender_address`, `amount_to_approve`, and `unlock_time` variables as needed.
4. Run the script using your preferred Python interpreter: `python script_name.py`.

Please exercise caution and ensure that you have a thorough understanding of the script's actions before using it. Unauthorized or incorrect transactions may result in irreversible loss of funds. Always test the script on a test network before using it on the mainnet.

**Disclaimer:** This script is provided as-is and does not constitute financial or investment advice. Use it at your own risk. The developers of this script are not responsible for any losses incurred.

**FeedBacK ADDRESS:  0xe93081718a75818Be2eB1E1336c8c2AC930e44e0**
