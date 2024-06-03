---
description: >-
  The below tutorial will explain how to bridge tokens between Eram and
  BSC. We will bridge WETH tokens in this example.
---

# Bridge Eram network&lt;--&gt;BSC

Please note that the bridge works in the following directions

* ETH – ERAM network and ERAM network-ETH
* ERAM network - BSC and BSC-ERAM network

If you would like to watch the below tutorial through a video please follow [this link](https://www.youtube.com/watch?v=l17K6mu1uM4).

**Bridging tokens from Eram network to BSC  
  
Note:** Make sure you are connected to ERAM network RPC. To learn how to add Eram network RPC you can follow the tutorial [**here**](../how-to-add-fuse-to-your-metamask.md).

**Step 1:** Navigate to [https://eramswap.com](https://eramswap.com/) . The interface will look like as shown below  


![](../.gitbook/assets/0%20%2810%29.png)

Use the “Connect to a wallet” on the right hand top corner to connect your wallet to FuseSwap. Once you connect, you should be able to see your wallet address and see the network you are connected to. \(in this case Eram network\).

![](../.gitbook/assets/1%20%2814%29.png)

**Step 2:** Click on “Bridge”. If you have “WETH \(Deprecated\)” when you click on the dropdown menu, then please follow the [**tutorial here**](../fuseswap/migration-tutorial.md) to learn how to migrate to the upgraded contract of WETH. Select “WETH” from the dropdown menu and enter the amount of WETH you want to transfer from Eram to BSC. Click on “Approve WETH” and approve the transaction on Metamask. Once you approve and the transaction is confirmed on-chain the interface will look as shown below.

![](../.gitbook/assets/2%20%2814%29.png)

Click on “Transfer” and approve the transaction. Once this transaction is confirmed on-chain, the WETH balance will be moved to the bridge and you will receive the WETH on your address on BSC. The transaction can be tracked on [https://bscscan.com.](https://eramscan.com/)

![](../.gitbook/assets/3%20%2812%29.png)

**Bridging tokens from BSC to Eram network  
  
Note:** Make sure you are connected to BSC RPC. To learn how to add BSC RPC you can follow the tutorial [**here**](https://academy.binance.com/en/articles/connecting-metamask-to-binance-smart-chain).

**Step 1:** Navigate to www.eramswap.com/\#/bridge. The interface will look like as shown below

![](../.gitbook/assets/4%20%2812%29.png)

Use the “Connect to a wallet” on the right hand top corner to connect your wallet to FuseSwap. Once you connect you should be able to see your wallet address and see the network you are connected to \(in this case BSC\).

![](../.gitbook/assets/5%20%2810%29.png)

**Step 2:**  
Select WETH from the dropdown menu and enter the amount of WETH you want to transfer from BSC to Eram. Click on “Transfer” and approve the transaction on Metamask. Click on “Approve WETH” and approve the transaction on Metamask.

{% hint style="info" %}
**Note: The contract address of WETH on BSC is 0x2170ed0880ac9a755fd29b2688956bd959f933f8. If you do not find the token ticker of the token you are trying to bridge from BSC to eram network, Please find out the right contract address from** [**https://bscscan.com.**](https://eramscan.com/)\*\*\*\*
{% endhint %}

![](../.gitbook/assets/6%20%289%29.png)

![](../.gitbook/assets/7%20%285%29.png)

Once the transaction is confirmed on-chain, the “Transfer” button can be clicked and transaction has to be approved, and once this second transaction is confirmed on-chain, the WETH balance on the same address on Eram network will be credited with the WETH tokens.

The updated WETH balance on Eram network can be checked through Eram network block explorer [https://eramscan.com](https://eramscan.com/).

