

# Employee Salary Tracker – Day XX

A decentralized application (dApp) for managing and tracking employee salaries on the blockchain. This project allows organizations to securely store employee details, update salaries, and provide transparent records, ensuring accountability and trust.

## 🚀 Features

### Core Functionality

* **Add Employee**: Register an employee with department, name, salary, wallet address, and gender.
* **Update Salary**: Modify the salary of a specific employee.
* **Departmental Organization**: Employees are stored in a mapping organized by department and name for easy lookup.

---

## 🛠 Smart Contract Details

**Contract Name**: `EmployeeSalaryTracker`
**Network**: Sepolia Testnet
**Solidity Version**: `0.8.19`
**License**: MIT
**Contract Address**:

```
0x33D31e56AC9D8Dfb35D6b35F602EF5cA131e0808
```

**Verified on Etherscan**: [View on Sepolia Etherscan](https://sepolia.etherscan.io/address/0x33D31e56AC9D8Dfb35D6b35F602EF5cA131e0808)

---

## 📜 Smart Contract Functions

### 1. **addEmployee**

```solidity
function addEmployee(string memory _department, string memory _name, uint256 _salary, address _walletAddress, string memory _gender) public
```

* Registers an employee in a department.
* Parameters:

  * `_department`: The department the employee belongs to.
  * `_name`: Employee name.
  * `_salary`: Initial salary in wei.
  * `_walletAddress`: Ethereum wallet address of the employee.
  * `_gender`: Gender of the employee.

---

### 2. **updateSalary**

```solidity
function updateSalary(string memory _department, string memory _name, uint256 _newSalary) public
```

* Updates the salary of a specific employee.
* Parameters:

  * `_department`: Department of the employee.
  * `_name`: Employee name.
  * `_newSalary`: New salary in wei.

---

## 🔗 Example Interactions

### Add an Employee

```javascript
await contract.addEmployee(
    "Engineering",
    "John Doe",
    ethers.utils.parseEther("2"), // Salary in ETH
    "0x1234...abcd",
    "Male"
);
```

### Update Salary

```javascript
await contract.updateSalary(
    "Engineering",
    "John Doe",
    ethers.utils.parseEther("3")
);
```

---

## 📦 Deployment & Verification

**Compile and Deploy** (via Hardhat or Remix) to Sepolia Network.
Example Hardhat command:

```bash
npx hardhat run scripts/deploy.js --network sepolia
```

**Verify on Etherscan**:

```bash
npx hardhat verify --network sepolia 0x33D31e56AC9D8Dfb35D6b35F602EF5cA131e0808
```

---

## 📌 Use Cases

* Payroll management in decentralized companies.
* Transparent salary tracking for DAOs.
* Immutable employee records stored on-chain.

---

