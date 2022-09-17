# ❓ FAQ

### **What is a Virtual Swap?**

Virtual swaps are a new feature in Jioswap pools leveraging Synthetix’s vSynths. With implementing vSynth logic in Jioswap's AMM, it’s possible to use synths as _bridges between pools for cross asset swaps_.&#x20;



### **What is Slippage?**

Slippage is the difference between the expected price of a trade and the execution price. This happens as there is a time delay between the trade request and execution in the market. Slippage can occur at any time but is amplified during periods of high volatility and with large volume trades.

In case of large trades, we recommend the use of aggregators like [1inch](https://1inch.io), [Matcha](https://matcha.xyz), or [Paraswap](https://paraswap.io) to limit the slippage.

### **What is Max Slippage?**

With max slippage setting, you can specify the maximum % of price movement you can accept for the trade. Your order will not execute if the slippage is beyond your maximum specified. The default for Jioswap is 0.1%, but you can set it to any % you want.
