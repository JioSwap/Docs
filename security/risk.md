# Risk

Providing liquidity to Jioswap is highly risky. Before using the protocol, we highly recommend reading the code and understanding the risks involved with being a Liquidity Provider (LP) and/or using the AMM to trade pegged value crypto assets.

Using Jioswap as an exchange user should be significantly less risky, but keep in mind there are still risks.



### Permanent loss of a peg

If one of the assets in a pool significantly depegs, it will effectively mean that pool liquidity providers will be left holding only that asset.

Reset token approval to 0 when having partial approval beforehand. As some tokens (eg. USDT) do not comply to ERC20 standards for `approve` function, when using limited approvals, you may have to reset the approvals to 0 before changing to another value. If gas usage is your concern, we recommend using unlimited approvals. Otherwise, we recommend using limited approvals for added security.

[ERC: Token standard · Issue #20 · ethereum/EIPs](https://github.com/ethereum/EIPs/issues/20#issuecomment-263524729)

###

###
