# DescentraSwap - Liquidity Management Protocol

![Solidity](https://img.shields.io/badge/Solidity-0.8.26-blue.svg)
![Foundry](https://img.shields.io/badge/Foundry-v0.2.0-orange.svg)
![Arbitrum](https://img.shields.io/badge/Arbitrum-One-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

DescentraSwap is a liquidity management protocol that allows interaction with SushiSwap on the Arbitrum network. It is specifically designed for swap operations and liquidity management between USDT and DAI.

## 🚀 Main Features

- **Automated Swap**: Efficient conversion between USDT and DAI
- **Liquidity Management**: 
  - Add liquidity to the USDT/DAI pool
  - Remove liquidity from the pool
  - Check LP token balances
- **Security**: 
  - Implementation of SafeERC20 for secure transfers
  - Configurable slippage control
  - Transaction deadlines

## 🛠 Technologies

- **Language**: Solidity 0.8.26
- **Framework**: Foundry
- **DEX**: SushiSwap V2
- **Network**: Arbitrum One
- **Dependencies**:
  - OpenZeppelin Contracts
  - SushiSwap Core
  - SushiSwap Periphery

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/Vicent00/LiquiSwap.git
cd LiquiSwap

```

2. Install the dependencies:
```bash
forge install
```

3. Configure the environment variables:
```bash
cp .env.example .env
# Edita .env con tus claves API
```

## 🧪 Testing

### Run Local Tests

```bash
forge test
```

### Run Tests on Arbitrum Fork
```bash
forge test --fork-url https://arb1.arbitrum.io/rpc -vvvv
```

### Generate Gas Report

```bash
forge test --gas-report
```


## 📚 Documentation

### Project Structure

```
LiquiSwap/
├── src/
│   ├── Swap.sol              # Contrato principal
│   └── interfaces/
│       ├── IRouter.sol       # Interfaz del Router
│       └── IFactory.sol      # Interfaz de la Factory
├── test/
│   └── testSwapLiquidity.t.sol  # Tests

└── lib/
    └── openzeppelin-contracts/
```

### Main Functions

#### Swap
```solidity
function swapTokens(
    uint amountIn_,
    uint amountOutMin_,
    address[] calldata path_,
    address to_,
    uint deadline_
) public
```

#### Add Liquidity

```solidity
function addLiquidity(
    uint amountUsdt_,
    uint amountDai_
) public returns (uint liquidity)
```

#### Remove Liquidity
```solidity
function removeLiquidity(
    uint amountLiquidity_
) public returns (uint amountA, uint amountB)
```

## 🔒 Security

- All token transfers use SafeERC20
- Implementation of the checks-effects-interactions pattern
- Reentrancy handling
- Deadline validation
- Slippage control

## 🤝 Contributing

- Fork the project
- Create your feature branch (`git checkout -b feature/AmazingFeature`)
- Commit your changes (`git commit -m 'Add some AmazingFeature'`)
- Push to the branch (`git push origin feature/AmazingFeature`)
- Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📞 Contact

- Email: info@vicenteaguilar.com

## 🙏 Acknowledgements

- SushiSwap team for their excellent DEX
- Arbitrum team for their L2 scaling solution
- Foundry community for their incredible toolkit

