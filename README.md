# 💰 Payment Splitter Smart Contract

## 🚀 Overview
The **PaymentSplitter** smart contract allows for the automatic distribution of Ether to multiple recipients based on predefined percentage shares. This contract can be used for revenue sharing, royalties, or other scenarios where payments need to be split among multiple parties.

## ✨ Features
- ✅ Hardcoded recipient addresses.
- ✅ Predefined percentage-based split of incoming Ether.
- ✅ Function to distribute received funds proportionally.
- ✅ No imports or constructors for simplicity.

## 🔍 How It Works
1. ⚡ The contract receives Ether through a transaction.
2. 📤 When `distribute()` is called, the contract calculates each recipient's share based on the predefined percentages.
3. 💸 The Ether is then transferred to each recipient accordingly.

## 📜 Contract Address
- 📌 **Deployed At:** `0x072a66fF61eDeC4CeBA08F3Df2C72f4364d72432`

## 📝 Code Explanation
- 📌 The `recipients` array stores three hardcoded payable addresses.
- 📌 The `shares` array defines the corresponding percentage allocation.
- 📌 The `distribute()` function:
  - 🏦 Retrieves the total Ether received in the transaction.
  - 🔄 Iterates through recipients and calculates their share.
  - 💵 Transfers the corresponding amount to each recipient.

## 📌 Usage
1. 📜 Deploy the contract on an Ethereum-compatible blockchain.
2. 💰 Send Ether to the contract.
3. 🏗️ Call the `distribute()` function to split and transfer funds.

## 📊 Example
If the contract receives **1 ETH**, the distribution will be:
- 🏦 **Recipient 1** (40%) → 0.4 ETH
- 🏦 **Recipient 2** (30%) → 0.3 ETH
- 🏦 **Recipient 3** (30%) → 0.3 ETH

## 🔐 Security Considerations
- ⚠️ Ensure the hardcoded recipient addresses are correct before deployment.
- ⚠️ The contract does not store Ether; it distributes it immediately upon function execution.

## 📜 License
This contract is open-source and free to use under the MIT License.

