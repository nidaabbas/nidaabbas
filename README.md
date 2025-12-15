# FundMe Smart Contract

A simple **FundMe** smart contract built with **Solidity** that allows users to fund the contract with ETH and lets the owner withdraw the funds. This project is commonly used to practice **Chainlink Price Feeds**, **Foundry**, and **smart contract testing**.

---

## 📌 Features

* Users can fund the contract using **ETH**
* Minimum funding amount enforced in **USD**
* Uses **Chainlink Price Feeds** to convert ETH → USD
* Only the **owner** can withdraw funds
* Gas‑optimized withdrawal function
* Fully testable using **Foundry**

---

## 🧠 How It Works (Simple Explanation)

1. User sends ETH to the `fund()` function
2. Contract checks if sent ETH is worth at least the **minimum USD value**
3. If valid, the user is added to the funders list
4. Owner can call `withdraw()` to transfer all ETH to their address

---

## 🛠 Tech Stack

* **Solidity** `^0.8.x`
* **Foundry** (Forge & Cast)
* **Chainlink Price Feeds**
* **Ethereum / Sepolia Testnet**

---

## 📂 Project Structure

```
FundMe/
│── src/
│   └── FundMe.sol
│── script/
│   └── DeployFundMe.s.sol
│── test/
│   └── FundMeTest.t.sol
│── lib/
│── foundry.toml
│── README.md
```

---

## ⚙️ Installation

```bash
forge init fund-me
cd fund-me
forge install smartcontractkit/chainlink-brownie-contracts
```

---

## 🚀 Deploy Contract

```bash
forge script script/DeployFundMe.s.sol \
  --rpc-url <YOUR_RPC_URL> \
  --private-key <YOUR_PRIVATE_KEY> \
  --broadcast
```

---

## 🧪 Run Tests

```bash
forge test
```

To see gas usage:

```bash
forge test --gas-report
```

---

## 🔐 Key Functions

### `fund()`

Allows users to send ETH if it meets the minimum USD value.

### `withdraw()`

Allows **only the owner** to withdraw all funds.

### `cheaperWithdraw()`

Gas‑optimized version of withdraw.

### `getVersion()`

Returns the Chainlink price feed version.

---

## ❗ Important Notes

* Minimum funding amount is defined in **USD**, not ETH
* Contract will revert if funding amount is too low
* Only owner can withdraw (uses `onlyOwner` logic)

---

## 🌱 Learning Outcomes

* Working with **Chainlink Oracles**
* Writing **secure smart contracts**
* Using **Foundry for testing & deployment**
* Understanding **gas optimization**

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🙌 Acknowledgements

Inspired by **Patrick Collins – Solidity & Foundry Course**.

---

### ✨ Author

Built with ❤️ while learning Blockchain & Smart Contract Security.

## ⚙️ Install
