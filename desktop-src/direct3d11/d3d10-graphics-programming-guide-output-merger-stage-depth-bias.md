---
title: 深度偏差
description: 在3D 空間中有共置的多邊形，會顯示為不是共置的多邊形，方法是將 z 偏差 (或深度偏差) 新增至每一個。
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684266"
---
# <a name="depth-bias"></a>深度偏差

在3D 空間中有共置的多邊形，會顯示為不是共置的多邊形，方法是將 z 偏差 (或深度偏差) 新增至每一個。

這項技術通常用來確保場景中的陰影正確顯示。 例如，牆上的陰影可能會有與牆相同的深度值。 如果應用程式先轉譯牆，然後再呈現陰影，則可能看不到陰影，或是可見的深度成品。


應用程式可以藉由將偏差 (從 D3D11 轉譯器) [**\_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)的 **DepthBias** 成員新增到系統在轉譯共置多邊形的集合時使用的 z 值，協助確保已正確轉譯共置多邊形。 具有較大 z 值的多邊形會繪製在具有較小 z 值的多邊形前方。

有兩個選項可計算深度偏差。

1.  如果目前系結至輸出合併階段的深度緩衝區有 **UNORM** 格式，或沒有系結的深度緩衝區，則偏差值的計算方式如下：
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    其中 *r* 是在深度緩衝區格式轉換為 **float32** 的最小可表示值 > 0。 **DepthBias** 和 **SlopeScaledDepthBias** 值是 D3D11 的轉譯器 [**\_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)結構成員。 **MaxDepthSlope** 值是圖元深度值水準和垂直傾斜的最大值。
2.  如果浮點深度緩衝區系結至輸出合併階段，偏差值的計算方式如下：
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    其中 *r* 是浮點數標記法中的尾數位數目 (不包括隱藏的位) ;例如，針對 **float32** 的23。

然後，偏差值會壓制如下：


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



然後，會使用偏差值來計算圖元深度。


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



深度偏差作業會在剪切之後頂點上發生，因此深度偏差不會影響幾何裁剪。 針對給定的基本值，偏差值是常數，而且會在插即置設定之前加入每個頂點的 z 值。 當您使用 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 和更高版本時，會使用32位浮點算術來執行所有偏差計算。 偏差不會套用到任何點或線條基本專案，但以線框模式繪製的線條除外。

具有陰影緩衝區型陰影的其中一個成品是陰影 acne，或是表面遮蔽本身，因為著色器中的深度計算和陰影緩衝區中的深度計算有些許差異。 解決這種情況的一種方法是在轉譯陰影緩衝區時使用 **DepthBias** 和 **SlopeScaledDepthBias** 。 其構想是在轉譯陰影緩衝區時，將表面推出足夠的範圍，讓陰影緩衝區 z 與著色器 z) 之間的比較結果 (一致，並避免本機自我遮蔽。

不過，使用 **DepthBias** 和 **SlopeScaledDepthBias** 時，可能會在以極銳利的角度查看的多邊形產生新的轉譯問題，而造成偏差方程式產生非常大的 z 值。 這實際上會從陰影地圖中的原始表面，將多邊形推播得相當遠。 解決此特定問題的其中一種方法是使用 **DepthBiasClamp**，它會在計算的 z 偏差範圍上提供上限 (正面或負面) 。

> [!Note]  
> 若為 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9.1、9.2、9.3、 **DepthBiasClamp** ，則不受支援。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輸出合併階段](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




