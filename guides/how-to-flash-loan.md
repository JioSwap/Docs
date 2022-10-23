# How to Flash-loan

Some of our pools allow flash-loaning assets for a small fee.

```
function flashLoan(
    address receiver,
    IERC20 token,
    uint256 amount,
    bytes memory params
) external;
```

Caller must provide a valid receiver address that inherits [IFlashLoanReceiver interface](https://github.com/JioSwap/jio-contracts/blob/dev/contracts/interfaces/IFlashLoanReceiver.sol).

```
function executeOperation(
    address pool,
    address token,
    uint256 amount,
    uint256 fee,
    bytes calldata params
) external;
```

Upon finishing `executeOperation`, the pool must have the initial liquidity back along with the associated fee. If the requirement is not met, then the transaction will fail.

We provide a [basic example of a flashloan borrower contract](https://github.com/JioSwap/jio-contracts/blob/dev/contracts/helper/FlashLoanBorrowerExample.sol).



## Do you have any flashloan countermeasures implemented?

For flashloan safety, we have 2 safety measures in place:

* Prevent reentrancy into the same pool. You cant flashloan money out of a pool and use that fund to trade through the same pool.
* Ensure the returned amount is always higher than borrowed amount. The transaction will revert if the borrower does not pay up by end of the transaction.

Our flash loan implementation is based on [Aave](https://aave.com/)'s [IFlashLoanReceiver.sol](https://github.com/aave/aave-protocol/blob/4b4545fb583fd4f400507b10f3c3114f45b8a037/contracts/flashloan/interfaces/IFlashLoanReceiver.sol).
