# 💻 Jio's Algorithm

Jio's StableSwap algorithm is based on a similar model as [Curve.Fi](https://curve.fi/) , which uses a hybrid function market maker algorithm (HFMM). see [AMM Defi Primer](https://deliverypdf.ssrn.com/delivery.php?ID=526026122121112000074075017075004004021019084010061003029097008119085101094126100098117019034042056022028000080068073005016117105078049036082099028106000089020093011024058017110080084090027095116122103008118014066071065096108101117116094008024126019020\&EXT=pdf\&INDEX=TRUE) for more info on this particular implementation. The hybrid function market maker (JIo's StableSwap )uses a combination of the Constant Product and Constant Sum implementation.\
\
When a particular pool is balanced, the algorithm functions as a **Constant Sum;** formula **x+y = k**

On the other hand as a particular pool on the platform becomes imbalanced , Jios algorithm functions as a **Constant Product**; formula : **x \* y = k**.
