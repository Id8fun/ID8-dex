# DEX (Decentralized Exchange)

This repository contains a simple implementation of a decentralized exchange (DEX) in Solidity. The DEX allows users to create liquidity pools, add liquidity, remove liquidity, and perform token swaps.
<br>

The DEX consists of two main smart contracts:
<br>
* **DEX.sol**: This contract serves as the main DEX contract and manages the creation of liquidity pools, providing and removing liquidity and token swaps.
* **LiquidityPool.sol**: This contract represents a liquidity pool within the DEX. It handles providing and removing liquidity and token swaps.

To use the DEX, follow these steps:
<br>
1. Deploy the DEX contract (DEX.sol) on the Ethereum network. Deployment should be done by running deployment script (set env variables before)

2. Call the ***createLiquidityPool*** function to create a new liquidity pool. Provide the addresses of the two tokens that will be traded in the pool, along with other parameters such as fee percentage and maximum swap percentage. This function will deploy a new ***LiquidityPool*** contract for the specified token pair.

3. Users can add liquidity to the liquidity pool by calling the ***addLiquidity*** function. Specify the token pair, the amounts of each token to be added, and the minimum amount of LP tokens to receive. This function transfers the tokens from the user to the liquidity pool and mints LP tokens representing their share of the pool.

4. Liquidity can be removed from the pool by calling the ***removeLiquidity*** function. Specify the token pair, the LP token amount to burn, and the minimum amounts of each token to receive. This function transfers the specified LP tokens from the user to the liquidity pool and returns the corresponding amounts of each token.

5. Token swaps can be performed by calling the ***swapExactInput*** or ***swapExactOutput*** functions. ***swapExactInput*** allows users to swap a specific amount of input token for an unspecified amount of output token, while ***swapExactOutput*** allows users to specify the desired amount of output token and receive an unspecified amount of input token. These functions utilize the liquidity pool to execute the swaps.

*Note: This implementation serves as a basic example and should not be used in production environments without thorough security audits and additional functionality.*

---

# DEX (去中心化交易所)

该仓库包含一个用 Solidity 实现的去中心化交易所（DEX）的简单版本。该 DEX 允许用户创建流动性池、添加流动性、移除流动性以及执行代币互换。
<br>

DEX 由两个主要的智能合约组成：
<br>
* **DEX.sol**：该合约作为主要的 DEX 合约，管理流动性池的创建、提供和移除流动性以及代币互换。
* **LiquidityPool.sol**：该合约代表 DEX 中的一个流动性池。它处理流动性的提供和移除以及代币互换。

使用 DEX 的步骤如下：
<br>
1. 在以太坊网络上部署 DEX 合约（DEX.sol）。部署应通过运行部署脚本完成（在此之前设置环境变量）。

2. 调用 ***createLiquidityPool*** 函数来创建一个新的流动性池。提供将在池中交易的两种代币的地址，以及其他参数，例如费用百分比和最大互换百分比。此函数将为指定的代币对部署一个新的 ***LiquidityPool*** 合约。

3. 用户可以通过调用 ***addLiquidity*** 函数向流动性池添加流动性。指定代币对、要添加的每种代币的数量以及要接收的最小 LP 代币数量。此函数将代币从用户转移到流动性池，并铸造代表其在池中份额的 LP 代币。

4. 可以通过调用 ***removeLiquidity*** 函数从池中移除流动性。指定代币对、要销毁的 LP 代币数量以及要接收的每种代币的最小数量。此函数将指定数量的 LP 代币从用户转移到流动性池，并返回相应数量的每种代币。

5. 代币互换可以通过调用 ***swapExactInput*** 或 ***swapExactOutput*** 函数来执行。***swapExactInput*** 允许用户互换特定数量的输入代币以获得不确定数量的输出代币，而 ***swapExactOutput*** 允许用户指定所需的输出代币数量并接收不确定数量的输入代币。这些函数利用流动性池来执行互换。

*注意：此实现仅作为基本示例，在未经彻底安全审计和附加功能的情况下，不应在生产环境中使用。*