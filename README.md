Talent Token (TLNT)

📌 Project Description

Talent Token (TLNT) is an ERC-20 token designed to reward users who contribute to the Talent verification system. Users earn TLNT tokens by actively participating in verification processes.

🚀 Features

Token Name: Talent

Symbol: TLNT

Standard: ERC-20

Total Supply: Defined at deployment

Authorization: Only the contract owner can mint new tokens

📜 Smart Contract Details

The contract is built using the OpenZeppelin ERC-20 library and includes the following functions:

Mint: Allows the owner to mint new tokens

Transfer: Enables users to send tokens to other addresses

BalanceOf: Checks the balance of a specific address

📦 Installation & Usage

To run the Talent Token in your environment, follow these steps.

1️⃣ Install Dependencies

npm install -g hardhat
npm install --save-dev @openzeppelin/contracts dotenv

2️⃣ Initialize Hardhat Project

npx hardhat

3️⃣ Deploy the Contract

To deploy on the Base network, run the following command:

npx hardhat run scripts/deploy.js --network base

📜 License

This project is released under the MIT license.

📧 Contact: For more details, visit the Talent Project repository.
